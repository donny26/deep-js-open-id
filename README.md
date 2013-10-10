deep-js-open-id
===============

An openID Package for deep-js


.loginWithExternalService



service config
```
{
  service: "weibo",
  clientId: "1292962797",
  secret: "75a730b58f5691de5522789070c319bc"
}
```
These functions initiate the login process with an external service (eg: Facebook, Google, etc), using OAuth. When called they open a new pop-up window that loads the provider's login page. Once the user has logged in with the provider, the pop-up window is closed and the Meteor client logs in to the Meteor server with the information provided by the external service.
In addition to identifying the user to your application, some services have APIs that allow you to take action on behalf of the user. To request specific permissions from the user, pass the requestPermissions option the login function. This will cause the user to be presented with an additional page in the pop-up dialog to permit access to their data. The user's accessToken — with permissions to access the service's API — is stored in the services field of the user document. The supported values for requestPermissions differ for each login service and are documented on their respective developer sites:

docs: 

* Facebook: http://developers.facebook.com/docs/authentication/permissions/
* GitHub: http://developer.github.com/v3/oauth/#scopes
* Google: https://developers.google.com/accounts/docs/OAuth2Login#scopeparameter
* Meetup: http://www.meetup.com/meetup_api/auth/#oauth2-scopes
* Twitter, Weibo: requestPermissions currently not supported
