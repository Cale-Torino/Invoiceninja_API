### Function Description
revoke a token

### Api Address 
https://www.techrad.co.za/apisource/public/authorization/revoke

### Payload
to revoke token `grant_type=revoke_token&revoke_token=b75a5c835478eff0693f-b701654be681e65caadff603ac6b5a0ffdf3d02841c3bf13-630f8aafde`

### Request Method 
- HTTP
- POST

### Request JSON Parameter (Input)
| parameters  |  type |  if required | description  | sample value  |
| :------------ | :------------ | :------------ | :------------ | :------------ |
|Authorization|String|required|auth|Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9|

#
### Response Parameter (Output)
| parameter  |  type | description  | sample value  |
| :------------ | :------------ | :------------ | :------------ |
|  success | bool | success parameter  | true|

### Response Results Example 
```json
{
  "success": true
}
```

---