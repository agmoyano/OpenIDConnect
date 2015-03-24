# Steps To Run Example

You must have [Node.js](http://nodejs.org/) and [Redis](http://redis.io/download) installed, and Redis must be running.

1. Fork this repository
2. Clone it, using your username

 ```
 git clone git@github.com:<YOUR_USERNAME>/OpenIDConnect.git
 cd OpenIDConnect
 ```

3. Install Node.js dependencies

 ```
 npm install
 cd examples
 npm install
 ```

4. Start server

 ```
 node openid-connect-example.js
 ```

5. Create user: http://localhost:3001/user/create
6. Register a client: http://localhost:3001/client/register
  * Client Key: exampleid
  * Redirect URI: http://localhost:3001/test
7. Test an auth flow at http://localhost:3001/test
  * Client Key: exampleid
  * Scopes: foo
  * Follow prompts
    - Accept
    - Get Token
    - Get Resource
    - You should see page that is restricted by ```foo``` scope
8. Logout: http://localhost:3001/logout?access_token=YOUR_ACCESS_TOKEN
9. Navigate to http://localhost:3001/user/foo?access_token=YOUR_ACCESS_TOKEN
