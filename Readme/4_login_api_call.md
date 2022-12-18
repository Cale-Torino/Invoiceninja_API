### Function Description
Login and get tokens

### Api Address 
https://www.techrad.co.za/apisource/public/consumer/login

### Payload
to login `{"username":"TestUser","password":"test1234"}`

Create the `username` and `password` via the fusio app [here](https://www.techrad.co.za/apisource/public/apps/fusio/#!/login)

however it's better to use the token (`authorization/token`) so you can revoke it later.

### username
`TestUser`

### password
`test1234`

### Request Method 
- HTTP
- POST

### Headers
| name  |  value | 
| :------------ | :------------ |
|Content-Type|application/json|

### Authentication
| name  |  value | 
| :------------ | :------------ |
|null|Bearer null|

### Request JSON Results Example
```json
//"Content-Type": "application/json"
{
  "method": "POST",
  "transformRequest": [
    null
  ],
  "transformResponse": [
    null
  ],
  "jsonpCallbackParam": "callback",
  "url": "https://www.techrad.co.za/apisource/public/consumer/login",
  "headers": {
    "Content-Type": "application/json",
    "Accept": "application/json, text/plain, */*"
  },
  "data": "{\"username\":\"TestUser\",\"password\":\"test1234\"}",
  "timeout": {}
}
```

### Response Parameter (Output)
| parameter  |  type   | description  | sample value  |
| :------------ | :------------ | :------------ | :------------ |
|  token | string | parameter list  | eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9 |
|  expires_in | int | parameter list  | 1657921976|
|  refresh_token | string | parameter list  | d74d652c7619210351b1-a0578ea1430e9e83f89e439538fa36b7103299d736b5275f-0848942e98|
|  scope | string | parameter list  | backend,backend.account,|

### Response Results Example
```json
{
  "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwczpcL1wvd3d3LnRlY2hyYWQuY28uemFcL2FwaXNvdXJjZVwvcHVibGljIiwic3ViIjoiNzVlMzhhZmItYjdmMS01ZjRiLWI4OGUtZTBhNDY4NmFjM2QyIiwiaWF0IjoxNjU3ODQ0MjE0LCJleHAiOjE2NTgwMTcwMTQsIm5hbWUiOiJUZXN0VXNlciJ9.a_8eiTuoFlcVcSlBfSp5MfMsOM9mA9Mrxkp6Lx2Mk7I",
  "expires_in": 1658017014,
  "refresh_token": "6c03f74b8dc767ae1f56-d90fcdb88b595415d3f5e68096b0c62d1077d5f74e9d316f-152be0e7f8",
  "scope": "backend,backend.account,backend.action,backend.app,backend.audit,backend.category,backend.config,backend.connection,backend.cronjob,backend.dashboard,backend.event,backend.log,backend.marketplace,backend.page,backend.plan,backend.rate,backend.role,backend.route,backend.schema,backend.scope,backend.sdk,backend.statistic,backend.transaction,backend.user,consumer,consumer.app,consumer.event,consumer.log,consumer.grant,consumer.page,consumer.plan,consumer.scope,consumer.subscription,consumer.transaction,consumer.user,authorization,my_scope"
}
```

---