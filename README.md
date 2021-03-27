# boot-oauth2-password-authorization
Authorization server spring boot 


URL POST : localhost:8080/oauth/token 
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
