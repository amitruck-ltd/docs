---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the Kittn API
---

# Introduction

Welcome to the Amitruck 2.0 API! You can use our API to access Amitruck API endpoints.

# Authentication

> To authorize, use this code:

```json
{
  "username": "John Doe",
  "password": "TestPassword3!"
}

```


```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: meowmeowmeow"
```


# Errors
Amitruck 2.0 uses the HTTP standards error codes. Below is the summary of the status to expect.
CODE | Description
--------- | -----------
20x | Everything went well
300 | Your request has been redirected
400 | The data submitted is invalid.
401 | Access Denied. Check Your credentials
403 | Forbidden. You don't have enough permissions
50x | Amitruck 2.0 internal error. Amitruck Engineers are notified.


# Customers
This section contains API related to customers such as customer's onboarding


# Transporters
This section contains API documentation related to transporters such as transporter's onboarding

# Drivers
This section contains API documentation for drivers

# Vehicles 
This section contains API documentation for vehicles

# Trips and Orders
This section cintains API documentatio for trips 

# Attendances 

# Fueling 

# Billing 