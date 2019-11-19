# @interactivefitness/strava-v3-client

## Installation

```bash
npm install @interactivefitness/strava-v3-client
```
## Description

This Strava API client was generated from Strava's official Swagger API spec. See the [Strava API playground](https://developers.strava.com/playground/) to see what's supported. Note that methods for the OAuth flow are not provided. 

## Quick start


```javascript

process.env.STRAVA_ACCESS_TOKEN = access_token
process.env.STRAVA_CLIENT_ID = client_id
process.env.STRAVA_CLIENT_SECRET = client_secret
process.env.STRAVA_REDIRECT_URI = redirect_uri

const strava = require("@interactivefitness/strava-v3-client")

strava
 .then(client => {
    if(client.errors) {
      throw new Error(client.errors);
    }
    return client.apis.Athletes.getLoggedInAthlete({})
 })
 .then(json => {
    console.log("got: ", json);
 });
 .catch(error => {
   console.error("error", error);
 });
```
