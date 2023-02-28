# oauth2-proxy + keycloak demo

This docker-compose setup demonstrates how to protect some web service behind an [oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy) + [keycloak](https://www.keycloak.org/) + DSFR authentification.

[![](./diagram.jpg)](https://developer.okta.com/blog/2022/07/14/add-auth-to-any-app-with-oauth2-proxy)

## Local dev setup

- Add `127.0.0.1   keycloak` to your `/etc/hosts`. this is necessary for the keycloak redirection
- Run `docker-compose up`
- Login to keycloak at `http://keycloak:8080` as `admin/admin` and create a new user in the `app-realm` realm, and check its "verified email" status.
- Try to login with your new user via http://127.0.0.1:3000

## Tips

- To signout from the target app, call `/oauth2/sign_out`
