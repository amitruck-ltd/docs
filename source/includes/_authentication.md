# Authentication

## User Registration
> Registration Request Payload:

```json
{
    "email": "testuser@amtruck.com",
    "phone_number": "+25470052355", 
    "names": "Test User",
    "password": "Qazwsxedcrfv123!",
    "password_confirm": "Qazwsxedcrfv123!"

}

```

> Registration Response Payload:

```json
{
    "status": "Success",
    "code": 201,
    "message": "Registration Successful",
    "data": [
        {
            "id": 37,
            "names": "Test User",
            "email": "testuser@amtruck.com",
            "phone_number": "+25470052355"
        }
    ]
}
```
Amitruck 2.0 APIs are grouped into two categories when it comes to authentication. Some require authentication others don't require authentication. **user registration** API does not require authentication. A user with access to the endpoint URL and has below payload can create register without being authenticated. 

This API allows you to register on Amitruck 2.0. Once the registration is successfully, an email will be sent do the user and you'll need to activate it by clicking on the activation link before the account can be activated on the system. 

Amitruck 2.0 is built around the SAAS concept, and each time the registration happens outside the invitation, the user team will be automatically created by the system, and the names of the person registering will be used as the team name. However the user has right to change the team name there after.

On a preffered client navigate to the Register endpoint with URL [https://dev.api.amitruck.co/v2/auth/user/register/](https://dev.api.amitruck.co/v2/auth/user/register/). The following are the request and response payload in JSON format.

Item | Value
---------- | -------
METHOD | POST 
URL | https://dev.api.amitruck.co/v2/auth/user/register/
HEADERS | Content-Type: "application/json"


## User Login

> Login Request Payload:

```json
{ 
    "email":"testtr@amtruck.com",
    "password": "Qazwsxedcrfv123!"
}

```

> Login Response Payload:

```json
{
    "status": "Success",
    "code": 200,
    "message": "Login Successful",
    "user_id": 36,
    "names": "Amitrurk User",
    "phone_number": "0700123127",
    "email": "testtr@amtruck.com",
    "permissions": ["account.add_emailconfirmation","account.change_emailconfirmation"],
    "current_team_id": 4,
    "refresh_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4c",
    "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNjcwMTM4Nz"
}
```

On a preffered client navigate to the Login endpoint with url [https://dev.api.amitruck.co/v2/auth/user/login/](https://dev.api.amitruck.co/v2/auth/user/login/). The following are the request and response payload in JSON format. This endpoint provides the Acccess token to be used to authenticate further requests.

Item | Value
---------- | -------
METHOD | POST 
URL | https://dev.api.amitruck.co/v2/auth/user/login/
HEADERS | Content-Type: "application/json"


## Change Password


> Change Password Request Payload:

```json
{
    "old_password": "Qazwsxedcrfv123!",
    "new_password": "Qazwsxedcrfv123!"
}
```
> Change Password Response Payload:

```json
{
    "status": "success",
    "code": 200,
    "message": "Password updated successfully",
    "data": []
}
```

On a preffered client navigate to the Login endpoint with url [https://dev.api.amitruck.co/v2/auth/user/change-password/](https://dev.api.amitruck.co/v2/auth/user/change-password/). The following are the request and response payload in JSON format. This endpoint require to be authenticated and the password of the authenticaded user will be updated.

Item | Value
---------- | -------
METHOD | POST 
URL | https://dev.api.amitruck.co/v2/auth/user/change-password/
HEADERS | Content-Type: "application/json"
AUTHORIZATION | Bearer Token

## Invite User

> Invite User Request Payload:

```json
{   "names":"Kamaro Lambert",
    "email": "kamaro@amitruck.com"
}
```
> Invite User Response Payload:

```json
{
    "status": "Success",
    "code": 201,
    "message": "Invitation Sent to User",
    "data": [
        {
            "id": 38,
            "names": "Kamaro Lambert",
            "email": "kamaro@amitruck.com"
        }
    ]
}
```

On a preffered client navigate to the Invite User endpoint with url [https://dev.api.amitruck.co/v2/auth/user/user-invite/](https://dev.api.amitruck.co/v2/auth/user/user-invite/). The following are the request and response payload in JSON format. This endpoint require to be authenticated and an invite will be sent to the user.

Item | Value
---------- | -------
METHOD | POST 
URL | https://dev.api.amitruck.co/v2/auth/user/user-invite/
HEADERS | Content-Type: "application/json"
AUTHORIZATION | Bearer Token

## Get All Users
> Invite User Request Payload:

```json
  none
```

> Invite User Response Payload:

```json
[
    {
        "id": 1,
        "names": "Amitruck Admin",
        "email": "admin2@amitruck.com",
        "phone_number": "07162352782"
    },
    {
        "id": 34,
        "names": "Amitruck Admin",
        "email": "admin@admin.com",
        "phone_number": "0757000000"
    }
]
```
On a preffered client navigate to the get all users endpoint with url [https://dev.api.amitruck.co/v2/auth/user/users/](https://dev.api.amitruck.co/v2/auth/user/users/). The following are the request and response payload in JSON format.

Item | Value
---------- | -------
METHOD | GET 
URL | https://dev.api.amitruck.co/v2/auth/user/users/
HEADERS | Content-Type: "application/json"
AUTHORIZATION | Bearer Token

## Login Otp
> Login Otp Response Payload:

```json
{ 
    "username":"testtr@amtruck.com"
}
```
> Login Otp Response Payload:

```json
{
    "status": "success",
    "code": 200,
    "message": "We've sent you an OTP to your email"
}
```
On a preffered client navigate to the Login Otp endpoint with url [https://dev.api.amitruck.co/v2/auth/user/login/otp/](https://dev.api.amitruck.co/v2/auth/user/login/otp/). The following are the request and response payload in JSON format. This request if successful will send an OTP to the user and will be used for authentication.

Item | Value
---------- | -------
METHOD | POST 
URL | https://dev.api.amitruck.co/v2/auth/user/login/otp/
HEADERS | Content-Type: "application/json"
AUTHORIZATION | Bearer Token




