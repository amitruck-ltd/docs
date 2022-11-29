# Authentication

With A valid Access token, we can use it to be able to access other API endpoints. We shall start by looking at the user register endpoint. On Post man navigate to the Register request with url [https://dev.api.amitruck.co/v2/auth/)user/register/](https://dev.api.amitruck.co/v2/auth/user/register/). The following are the request and response payload in JSON format.

With A valid Access token, we can use it to be able to access other API endpoints. We shall start by looking at the user register endpoint. On Post man navigate to the Register request with url https://dev.api.amitruck.co/v2/auth/user/register/. The following are the request and response payload in JSON format.

With A valid Access token, we can use it to be able to access other API endpoints. We shall start by looking at the user register endpoint. On Post man navigate to the Register request with url https://dev.api.amitruck.co/v2/auth/user/register/. The following are the request and response payload in JSON format.

With A valid Access token, we can use it to be able to access other API endpoints. We shall start by looking at the user register endpoint. On Post man navigate to the Register request with url https://dev.api.amitruck.co/v2/auth/user/register/. The following are the request and response payload in JSON format.

With A valid Access token, we can use it to be able to access other API endpoints. We shall start by looking at the user register endpoint. On Post man navigate to the Register request with url https://dev.api.amitruck.co/v2/auth/user/register/. The following are the request and response payload in JSON format.

> Registration Request Payload:

```json
{
    "email": "test@amitruck.com",
    "phone_number": "254700500200",
    "names": "Amitrurk User",
    "password": "Test1234",
    "password_confirm": "Test1234"

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
            "id": 3,
            "names": "Amitrurk User",
            "email": "test@amitruck.com",
            "phone_number": "254700500200"
        }
    ],
    "token": "7f82a49e98030b4476858786a3f3ebac274b6ca4a87691e21696dfe15b6a1431"
}
```