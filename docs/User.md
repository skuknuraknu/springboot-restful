# User API Spec

## Register User

- Endpoint: POST /api/user

Request Body:
```json
{
  "username": "",
  "password": "",
  "name": "Nayla"
}
```
Response Body:
```json
{
  "success": true,
  "data":[]
}
```
Respose Body(Error):
```json
{
  "success": false,
  "errors": []
}
```
## Login User

- Endpoint: POST /api/auth/login

Request Body:
```json
{
  "username": "",
  "password": ""
}
```
Response Body:
```json
{
  "success": true,
  "data":{ "_token": "xxx", "expireAt": 2336442144 }
}
```
Response Body(Error):
```json
{
  "success": false,
  "errors": []
}
```

## Get User

- Endpoint: GET /api/users/current

Request Header:
- X-API-TOKEN: Token (Mandatory)

Response Body:
```json
{
  "success": true,
  "data":{ "userdata": {} }
}
```
Response Body(Error):
```json
{
  "success": false,
  "errors": []
}
```

## Update User

- Endpoint: PUT /api/users/current

Request Header:
- X-API-TOKEN: Token (Mandatory)

Request Body:
```json
{
  "name": "",
  "password": ""
}
```
Response Body:
```json
{
  "success": true,
  "data":{ }
}
```
Response Body(Error):
```json
{
  "success": false,
  "errors": []
}
```

## Logout User
- Endpoint: DELETE /api/auth/logout

Request Header:
- X-API-TOKEN: Token (Mandatory)

Response Body:
```json
{
  "success": true,
  "data":{ }
}
```