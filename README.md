# auth-ldap - LDAP Authentication module for nginx

LDAP module for nginx which supports authentication against multiple LDAP servers.

## Project history

This project is a fork of [Ericbla/nginx-auth-ldap](https://github.com/Ericbla/nginx-auth-ldap), itself a derived module from [kvspb](https://github.com/kvspb/nginx-auth-ldap)'s.

The reasons for this (other) fork are:

- very same reasons as forked project
- to adapt it to fit my own project constraints and needs, mainly:
  - return all values for each searched attribute in a header, not only the first value - used to get a list of all groups a user belongs to
  - provide a `ngx_array_t *auth_ldap_get_attributes(ngx_http_request_t *r)` to get all those attributes directly

## Build… build???

If you need a "generic" LDAP authentication nginx module, you probably don't need this one. Try one of the other modules listed above and you will find how to build.

This module is actually used as a submodule of another project of mine: [dav-next](https://codeberg.org/lunae/dav-next). Check this out!

If you really need this very module, you already know how to build it.

## Extra LDAP schema file

`lunae.schema` is a schema file that contains, among other, the LDAP attribute definition of `gid` used, for now, by this module.

## Last words

I don't plan for now to send upstream my changes be cause they may not be useful in their context, however I plan to (mostly manually) merge their new commits if they make sense in this context.
