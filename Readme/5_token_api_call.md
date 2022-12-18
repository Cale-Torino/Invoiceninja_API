### Function Description
Get auth token or refresh token

### Api Address 
https://techrad.co.za/apisource/public/authorization/token

### Payload
to login `grant_type=client_credentials`
to refresh `grant_type=refresh_token&refresh_token=b75a5c835478eff0693f-b701654be681e65caadff603ac6b5a0ffdf3d02841c3bf13-630f8aafde`
Authorization Token Grant from Refresh Token `grant_type=refresh_token&refresh_token=[token]&client_id=[app_key]&client_secret=[app_secret]`
Authorization Token Grant from Authorization Code `grant_type=authorization_code&code=[code]&client_id=[app_key]&redirect_uri=[redirect_uri]&client_secret=[app_secret]`

### Request Method 
- HTTP
- POST

### Request JSON Parameter (Input)
| parameters  |  type |  if required | max length  | description  | sample value  |
| :------------ | :------------ | :------------ | :------------ | :------------ | :------------ |
|APPKEY/username|String|required|20|username or appkey id|40bfc7b2-9c23-49a1-822e-e7028bd5538d|
|APPSECRET/password|String|required|20|password or appsecret|a2c832d077419d5a1d00180b9a524c6c73f1315536b2d4ab30ffc814afc61598|

`APPKEY/username` and `APPSECRET/password` must be `base64encoded` and placed in Authorization header

E.G: 
- `{appkey}:{appsecret}` or `{username}:{password}`
- `40bfc7b2-9c23-49a1-822e-e7028bd5538d:a2c832d077419d5a1d00180b9a524c6c73f1315536b2d4ab30ffc814afc61598`

Then they become `"Authorization": "Basic NDBiZmM3YjItOWMyMy00OWExLTgyMmUtZTcwMjhiZDU1MzhkOmEyYzgzMmQwNzc0MTlkNWExZDAwMTgwYjlhNTI0YzZjNzNmMTMxNTUzNmIyZDRhYjMwZmZjODE0YWZjNjE1OTg=",`

base64 encoded

### Request Results Example 
```
Accept	application/json, text/plain, */*
Authorization	Basic NDBiZmM3YjItOWMyMy00OWExLTgyMmUtZTcwMjhiZDU1MzhkOmEyYzgzMmQwNzc0MTlkNWExZDAwMTgwYjlhNTI0YzZjNzNmMTMxNTUzNmIyZDRhYjMwZmZjODE0YWZjNjE1OTg=
Content-Type	application/x-www-form-urlencoded
```

### Response Parameter (Output)
| parameter  |  type   | description  | sample value  |
| :------------ | :------------ | :------------ | :------------ |
|  access_token | string | parameter list  | eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9 |
|  token_type | string  | parameter list  | bearer <br>|
|  expires_in | int | parameter list  | 1657921976|
|  refresh_token | string | parameter list  | d74d652c7619210351b1-a0578ea1430e9e83f89e439538fa36b7103299d736b5275f-0848942e98|
|  scope | string | parameter list  | my_scope|

### Response Results Example 
```json
{
  "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwczpcL1wvd3d3LnRlY2hyYWQuY28uemFcL2FwaXNvdXJjZVwvcHVibGljIiwic3ViIjoiNzVlMzhhZmItYjdmMS01ZjRiLWI4OGUtZTBhNDY4NmFjM2QyIiwiaWF0IjoxNjU3ODA1ODgzLCJleHAiOjE2NTc5Nzg2ODMsIm5hbWUiOiJUZXN0VXNlciJ9.oyX-HAe3g6RcaSj0lxXNFA8p1JYRFg9xAuSr0b8NIes",
  "token_type": "bearer",
  "expires_in": 1657978683,
  "refresh_token": "6698a0b9b07e21347027-b877dad7579840c7b3d2e27959d9a9d91dc626b41c8a7704-8d33a40f63",
  "scope": "my_scope"
}
```

---