
### Function Description
TEMPLATE

### Api Address 
/user/save.do

### Request Method 
- HTTP 
- GET 
- POST

### Request Parameter (Input)
| parameters  |  type |  if required | max length  | description  | sample value  |
| :------------ | :------------ | :------------ | :------------ | :------------ | :------------ |
|id|String|required|20|user id|1|
|name|String|required|20|user name|gege|
|linkMan|String|required|20|contact|gege|
|telephone|String|required|20|phone|12345678901|
|email|String|required|20|e-mail|2222@qq.com|
|url|String|required|20|website|www.baidu.com|
|unetworkTrafficLimitationrl|String|required|20|max traffic|200|

#
### Response Parameter (Output)
| parameter  |  type |  max length  | description  | sample value  |
| :------------ | :------------ | :------------ | :------------ | :------------ |
|  result | list |  0  | parameter list  | 29 named already used <br> 16 user info doesn't existed <br>|

### Response Results Example 
```json
{result:0}
```