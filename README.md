# auth-google

Command line helper tool to work with Google access tokens.

## Installation

```bash
$ npm install auth-google --save
```

```JavaScript
require('auth-google')({
      name: 'my-app' // will be used to store the token under ~/.config/my-app/token.json
    , client_id: '...' // enter client id from the developer console
    , client_secret: '...' // enter client secret from the developer console
    , scope: [] // add scopes 
}, function (error, token) {
    // token.access_token - your token
    // token.token_type - token type
    // token.expires_at - timestamp when this token will be expired
    // token.refresh(callback) - Refreshes the token
});
```
