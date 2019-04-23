### About
OAuth 2 authorization server

#### Prerequisites
* Java 11

##### Example
request
```
curl -X POST \
  http://localhost:8080/oauth/token \
  -H 'Authorization: Basic U3RyZXhDb3JwOnNtaWxpbmdfZ29k' \
  -d 'username=john&password=theFarmerPass&grant_type=password'
```
response
```
{
    "access_token": "3c369ded-7a34-4c64-ae93-7c0b0b875726",
    "token_type": "bearer",
    "refresh_token": "356f5fa0-8e16-4d4c-a5dd-44e0f2e28383",
    "expires_in": 43199,
    "scope": "read write"
}
```