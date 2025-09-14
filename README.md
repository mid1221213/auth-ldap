# LDAP Authentication module for nginx

LDAP module for nginx which supports authentication against multiple LDAP servers.

## Project history

This project is a fork of [nginx-auth-ldap](https://github.com/Ericbla/nginx-auth-ldap), itself a derived module from [kvspb](https://github.com/kvspb).

The reasons for this (another) fork are:

- Same reasons as (what I call here) "upstream" (Ericbla/nginx-auth-ldap)
- Adapt it to fit my own project constraints and needs, mainly:
  - return all values for each searched attribute in a header, not only the first value - used to get a list of all groups a user belongs to
  - provide a `ngx_array_t *auth_ldap_get_attributes(ngx_http_request_t *r)` to get all those attributes directly
