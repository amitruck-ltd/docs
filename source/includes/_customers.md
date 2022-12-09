# CUSTOMER ONBOARDING SERVICE

This section contains API related to customers such as customer's onboarding

> Corporate Customer Registration Request Payload:

```json
{
  "contact_person_names": "John Doe",
  "contact_person_email": "johndoe@remotework.com",
  "contact_person_phone": "254757161010",
  "contact_person_role": "Sales manager",
  "company_name": "RemoteWork",
  "company_website": "remotework.com",
  "company_phone": "254710000000",
  "company_location": "Longitude;latidude",
  "password": "TestPassword1!",
  "password_confirm": "TestPassword1!",
  "terms_and_condition_accepted": 1
}
```

> Corporate Customer Registration Response Payload:

```json
{
  "code": 201,
  "status": "success",
  "description": "Corporate Customer Registered Successfully. Verification Email and SMS Sent",
  "data": [
    {
      "id": 1,
      "registration_type": "Business",
      "contact_person_names": "John Doe",
      "contact_person_email": "johndoe@remotework.com",
      "contact_person_phone": "254757161010",
      "contact_person_role": "Sales manager",
      "company_name": "RemoteWork",
      "company_website": "remotework.com",
      "company_phone": "254710000000",
      "company_location": "Longitude;latidude",
      "password": "TestPassword1!",
      "password_confirm": "TestPassword1!",
      "terms_and_condition_accepted": 1,
      "current_team_id": 2,
      "success_at": "2022-11-09T11:43:21",
      "updated_at": "2022-11-09T11:43:21",
      "tc_accepted_at": "2022-11-09T11:43:21"
    }
  ]
}
```

Amitruck 2.0 APIs are grouped into two categories when it comes to authentication. Some require authentication others don't require authentication. **Customer registration** API does not require authentication. A customer with access to the endpoint URL and has below payload can create register without being authenticated.

This API allows you to register on Amitruck 2.0 as a customer. Once the registration is successfully, an email will be sent do the customer and you'll need to activate it by clicking on the activation link before the account can be activated on the system.

Amitruck 2.0 is built around the SAAS concept, and each time the registration happens outside the invitation, the user team will be automatically created by the system, and the names of the person registering will be used as the team name. However the user has right to change the team name there after.

On a preffered client navigate to the Register endpoint with URL [https://dev.api.amitruck.co/v2/customers/register/](https://dev.api.amitruck.co/v2/customers/register/). The following are the request and response payload in JSON format.

| Item    | Value                                              |
| ------- | -------------------------------------------------- |
| METHOD  | POST                                               |
| URL     | https://dev.api.amitruck.co/v2/customers/register/ |
| HEADERS | Content-Type: "application/json"                   |

> Individual Customer Registration Request Payload:

```json
{
  "names": "John Doe",
  "email": "johndoe@amitruck.com",
  "phone_number": "254757161010",
  "password": "Test1234",
  "password_confirm": "Test1234",
  "accepted_terms_and_condition": 1
}
```

> Individual Customer Registration Response Payload:

```json
{
  "code": 201,
  "status": "success",
  "description": "Customer Registered Successfully. Verification Notifications are sent successfully",
  "data": [
    {
      "id": 1,
      "names": "John Doe",
      "email": "johndoe@amitruck.com",
      "phone_number": "254757161010",
      "registration_type": "individual",
      "current_team_id": 3,
      "accepted_terms_and_condition": 1,
      "success_at": "2022-11-09T11:09:54",
      "updated_at": "2022-11-09T11:09:54",
      "tc_accepted_at": "2022-11-09T11:09:54"
    }
  ]
}
```
