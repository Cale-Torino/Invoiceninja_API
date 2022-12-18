

/developer/auth?response_type=code&client_id=[app_key]&redirect_uri=[redirect_uri]&scope=[scopes]

/consumer/account/change_password

/consumer/password_reset

### Function Description
Developer auth

### Api Address 
https://www.techrad.co.za/apisource/public/developer/auth

### Request Method 
- HTTP
- GET

### Request JSON Parameter (Input)
| name  |  value | 
| :------------ | :------------ |
|null|null|

### Headers
| name  |  value | 
| :------------ | :------------ |
|Content-Type|application/x-www-form-urlencoded|
|nUser-Agentame|Fusio TestCase|

### Authentication
| name  |  value | 
| :------------ | :------------ |
|Authentication|Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9|

### Request JSON Results Example 
```json
{
  "method": "GET",
  "transformRequest": [
    null
  ],
  "transformResponse": [
    null
  ],
  "jsonpCallbackParam": "callback",
  "url": "https://www.techrad.co.za/apisource/public/authorization/whoami",
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "User-Agent": "Fusio TestCase",
    "Authorization": "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwczpcL1wvd3d3LnRlY2hyYWQuY28uemFcL2FwaXNvdXJjZVwvcHVibGljIiwic3ViIjoiNzVlMzhhZmItYjdmMS01ZjRiLWI4OGUtZTBhNDY4NmFjM2QyIiwiaWF0IjoxNjU3ODQxNDEzLCJleHAiOjE2NTgwMTQyMTMsIm5hbWUiOiJUZXN0VXNlciJ9.Q-SWVNsNIN92tcX59iS_1SnTwzTo2qGOvRzNrOBqc60",
    "Accept": "application/json, text/plain, */*"
  },
  "data": "",
  "timeout": {}
}
```

### Response Parameter (Output)
| parameter  |  type | description  | sample value  |
| :------------ | :------------ | :------------ | :------------ |
|  id | int | id no | 1|
|  roleId | int | id no | 1|
|  status | int | id no | 1|
|  name | string | id no | TestUser|
|  email | string | id no | test@iq-blue.com|
|  scopes | array | id no | "consumer","consumer.app",|
|  date | string | id no | 2022-07-13T21:23:37Z|

### Response Results Example 
```json
{
  "id": 3,
  "roleId": 3,
  "status": 1,
  "name": "TestUser",
  "email": "test@iq-blue.com",
  "scopes": [
    "consumer",
    "consumer.app",
    "consumer.event",
    "consumer.log",
    "consumer.grant",
    "consumer.page",
    "consumer.plan",
    "consumer.scope",
    "consumer.subscription",
    "consumer.transaction",
    "consumer.user",
    "authorization",
    "my_scope"
  ],
  "date": "2022-07-13T21:23:37Z"
}
```