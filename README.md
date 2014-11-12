##goklp: Golang OpenSSH Keys Ldap Provider for AuthorizedKeysCommand

###Usage:
1. Setup goklp.ini - must be in same directory as goklp
1. Test to ensure goklp returns SSH keys: goklp <username>
1. Add this line to your sshd_config: AuthorizedKeysCommand /path/to/goklp

###goklp.ini config file is required:

```
goklp_ldap_uri          = ldaps://server1:636,ldaps://server2:636   (required)
goklp_ldap_bind_dn      = CN=someuser,O=someorg,C=sometld           (required)
goklp_ldap_base_dn      = O=someorg,C=sometld                       (required)
goklp_ldap_bind_pw      = someSecretPassword                        (required)
goklp_ldap_timeout_secs = 10                           (optional - default: 5)
goklp_debug             = false                    (optional - default: false)
```
