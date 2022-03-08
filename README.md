# OpenLDAP tips and tricks

First install openldap-clients on a linux server that can access the LDAP server via the network.
```
sudo dnf install openldap-clients
```

hostname:port below is something like denodo-host:389 or 192.168.56.102:389

# Find all info:
```
ldapsearch -LLL -x -H ldap://<hostname:port> | less
```
# Find a user by name:
```
ldapsearch -LLL -x 'cn=Adam Horivitz' -H ldap://<hostname:port>
```
# Find a user by name with wildcard:
```
ldapsearch -LLL -x 'cn=*Horivitz' -H ldap://<hostname:port>
```
or
```
ldapsearch -LLL -x 'cn=Adam*' -H ldap://<hostname:port>
```
or even
```
ldapsearch -LLL -x 'cn=*Horiv*' -H ldap://<hostname:port>
```
See manpage examples of ldapmodify to see how to modify a user with LDIF files.
