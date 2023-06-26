# Role Letsencrypt Remote
This role requests certificates via DNS TXT record challanges setup by using DNS providers APIs. It runs on the remote host.

This role was written for Debian 11 servers.


# Example play
```yaml
- hosts: all
  roles:
    - blunix_role-letsencrypt-remote_11.0.0
  vars:

    # List of domains
    letsencrypt_domain_names:
      - "my.domain.com"

    # Which "plugin" under plays/plugins/ to use
    letsencrypt_plugin: luadns

    # shell task to execute on the server after renewing the certificate
    letsencrypt_post_hook: service apache2 restart

    # Maximum certificate age in days before renewal is triggered
    letsencrypt_renew_days_max: 80
```

# License
Apache-2.0

# Author Information
Service and support for orchestrated hosting environments, continuous integration/deployment/delivery and various Linux
and open-source technology stacks are available from:

```
Blunix GmbH - Professional Linux Service
Glogauer Straße 21
10999 Berlin - Germany

Web: www.blunix.org
Email: mailto:service@blunix.org
```
