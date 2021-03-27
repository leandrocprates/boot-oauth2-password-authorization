# boot-oauth2-password-authorization
Authorization server spring boot 

Collection PostMan no diretorio : src/main/resources/collection_postman  


URL POST : http://localhost:8080/oauth/token 
```
Basic Auth : 
  username : javainuse-client 
  password : javainuse-secret
```
```
Body : 

grant_type : password
username : javainuse-user 
password : javainuse-pass
```

Resposta : 
```json
{
    "access_token": "e296d454-1a42-4a02-9a1e-073d9dbdd873",
    "token_type": "bearer",
    "refresh_token": "5931191e-8df0-4cb9-91f1-da5a096f6ae9",
    "expires_in": 40727,
    "scope": "read write"
}

```


URL GET : http://localhost:8080/validateUser 
```
Header 
    Authorization : Bearer 0a23fb2e-2c1d-4450-a9e1-e5b759880d99
``` 

Passar token do retorno ao serviço "oauth/token"

Resposta : 

```json
{
  "details": {
    "remoteAddress": "0:0:0:0:0:0:0:1",
    "sessionId": null,
    "tokenValue": "0a23fb2e-2c1d-4450-a9e1-e5b759880d99",
    "tokenType": "Bearer",
    "decodedDetails": null
  },
  "authorities": [
    {
      "authority": "ROLE_USER"
    }
  ],
  "authenticated": true,
  "userAuthentication": {
    "details": {
      "grant_type": "password",
      "username": "javainuse-user"
    },
    "authorities": [
      {
        "authority": "ROLE_USER"
      }
    ],
    "authenticated": true,
    "principal": {
      "password": null,
      "username": "javainuse-user",
      "authorities": [
        {
          "authority": "ROLE_USER"
        }
      ],
      "accountNonExpired": true,
      "accountNonLocked": true,
      "credentialsNonExpired": true,
      "enabled": true
    },
    "credentials": null,
    "name": "javainuse-user"
  },
  "oauth2Request": {
    "clientId": "javainuse-client",
    "scope": [
      "read",
      "write"
    ],
    "requestParameters": {
      "grant_type": "password",
      "username": "javainuse-user"
    },
    "resourceIds": [],
    "authorities": [],
    "approved": true,
    "refresh": false,
    "redirectUri": null,
    "responseTypes": [],
    "extensions": {},
    "refreshTokenRequest": null,
    "grantType": "password"
  },
  "credentials": "",
  "clientOnly": false,
  "principal": {
    "password": null,
    "username": "javainuse-user",
    "authorities": [
      {
        "authority": "ROLE_USER"
      }
    ],
    "accountNonExpired": true,
    "accountNonLocked": true,
    "credentialsNonExpired": true,
    "enabled": true
  },
  "name": "javainuse-user"
}

```
