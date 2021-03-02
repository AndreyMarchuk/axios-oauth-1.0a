
Fork differences:
- axios version update 
- added following params
```js
 /**
   * Include the OAuth params into url
   */
  includeIntoURL?: boolean | false;

  /**
   * OAuth callback param (optional)
   */
  callback?: string | null;
```

To sign your axios requests using OAuth 1.0a:

```js
import addOAuthInterceptor from 'axios-oauth-1.0a';

// commonjs way to import
// const addOAuthInterceptor = require('axios-oauth-1.0a').default

// Create a client whose requests will be signed
const client = axios.create();

// Add interceptor that signs requests
addOAuthInterceptor(client, {
  // OAuth consumer key and secret
  key: "xxx",
  secret: "yyy",
 
  // HMAC-SHA1 and HMAC-SHA256 are supported
  algorithm: "HMAC-SHA1",
});
 
// Now send requests to the OAuth 1.0a service using that client

```

## BUILD

build the package

`npm install -g typescript`
`npm i --save-dev @types/node`
`cd axios-oauth-1.0a`
`npm run build`
