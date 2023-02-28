# oauth2-proxy + keycloak demo

This docker-compose setup demonstrates how to protect some web service behind an [oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy) + [keycloak](https://www.keycloak.org/) authentification

## KeyCloak setup

- Create new client in your Keycloak realm with Access Type 'confidental', Client protocol 'openid-connect' and Valid Redirect URIs 'https://internal.yourcompany.com/oauth2/callback'
- Take note of the Secret in the credential tab of the client
- Create a mapper with Mapper Type 'Group Membership' and Token Claim Name 'groups'.
- Create a mapper with Mapper Type 'Audience' and Included Client Audience and Included Custom Audience set to your client name.
