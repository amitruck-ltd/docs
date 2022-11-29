# Authentication


## User Registration
On a preffered client navigate to the Register request with url [https://dev.api.amitruck.co/v2/auth/user/register/](https://dev.api.amitruck.co/v2/auth/user/register/). The following are the request and response payload in JSON format.
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

## User Login
On a preffered client navigate to the Login request with url [https://dev.api.amitruck.co/v2/auth/user/login/](https://dev.api.amitruck.co/v2/auth/user/login/). The following are the request and response payload in JSON format. This endpoint provides the Acccess token to be used to authenticate further requests.


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



## Change Password

## Invite User

## Get All Users

## Login Otp

## User Registration



