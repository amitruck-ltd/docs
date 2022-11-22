# Transporters
This section contains API documentation related to transporters such as transporter's onboarding

# Errors

Amitruck 2.0 uses the HTTP standards error codes. Below is the summary of the status to expect.

The Amitruck 2.0 API uses the following error codes:


Error Code | Meaning
---------- | -------
20x | Everything went well
400 | Bad Request -- Your request is invalid.
401 | Unauthorized -- Your API key is wrong.
403 | Forbidden -- The kitten requested is hidden for administrators only.
404 | Not Found -- The specified kitten could not be found.
405 | Method Not Allowed -- You tried to access a kitten with an invalid method.
406 | Not Acceptable -- You requested a format that isn't json.
410 | Gone -- The kitten requested has been removed from our servers.
418 | I'm a teapot.
429 | Too Many Requests -- You're requesting too many kittens! Slow down!
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
