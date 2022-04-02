# A simple node that sends templated e-mails with AWS Simple Email Service.

## Pre-requisites
1. You need to have a account on AWS and create a programatic access user on IAM with permission to send e-mail with AWS Simple Email Service.
2. You need to follow the steps to configure the SES with a verified domain to send emails.

## Configure the node
Double click the node and fill all fields

## Payload
It expects a payload with these properties;

- payload.recipient: Email address to sendo to, should be valid and accept just one address at time.
- payload.subject: The email subject, should be short string.
- payload.template: The template name created on AWS SES.
- payload.templateData: A list of replacement values to apply to the template (stringified JSON).

## Return
It returns an Object with the Id of the email sended

```
{
    "ResponseMetadata":{
        "RequestId":"d05b47cf-0ee2-413f-b06b-fe981fbfed1b"
    },
    "MessageId":"0101017599fe549f-64676c3d-8dda-478b-9765-228d49de341c-000000"
}
```
    