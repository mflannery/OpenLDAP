# OpenLDAP tips and tricks

# Find all info:
```
ldapsearch -LLL -x -H ldap://<hostname:port> | less
```
# Find a user by name:
```
ldapsearch -LLL -x 'cn=Adam Horivitz' -H ldap://denodo-host:389
```
# Find a user by name with wildcard:
```
ldapsearch -LLL -x 'cn=*Horivitz' -H ldap://denodo-host:389
```
or
```
ldapsearch -LLL -x 'cn=Adam*' -H ldap://denodo-host:389
```
See manpage examples of ldapmodify to see how to modify a user with LDIF files.
