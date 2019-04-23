### About
OAuth 2 authorization server

#### Prerequisites
* Java 11

##### Example

* access token

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
* refresh token

request

```
curl -X POST \
  http://localhost:8080/oauth/token \
  -H 'Authorization: Basic U3RyZXhDb3JwOnNtaWxpbmdfZ29k' \
  -d 'grant_type=refresh_token&client_id=StrexCorp&refresh_token=99540798-83b0-4b12-ab2c-e786dc4936c7'
```
response
```
{
    "access_token": "d17a0788-a34d-4d07-aa51-839f3b7416c7",
    "token_type": "bearer",
    "refresh_token": "99540798-83b0-4b12-ab2c-e786dc4936c7",
    "expires_in": 43199,
    "scope": "read write"
}
```