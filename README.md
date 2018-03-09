# Google-API-Token-Generator
Generates access_tokens for Google API, also generates refresh_token which can be used for refreshing access_tokens on server side later w/o OAuth2 prompt.

* Create OAuth2 credentials(type:`Other`):
  https://console.developers.google.com/apis/credentials

* Download json file and rename to client_secret.json and place in `./` root app dir.

* Run `node app.js`

* Go to URL provided, authorize with your Google account using OAuth2 and copy result code

* Paste in terminal and hit enter

* Copy generated entire token JSON file

* You can use this token on server side w/o any more user interaction

* Access_token will expire in 1 hour (as opposed to 5 minutes for `online` tokens), which is still not acceptable because we want to true permanent/long lived token.
As long as we have `refresh_token` we can refresh `access_token` with just 1 line of code: https://github.com/google/google-api-nodejs-client/#manually-refreshing-access-token
