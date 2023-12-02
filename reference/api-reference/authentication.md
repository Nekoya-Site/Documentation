# Authentication

## Register

{% swagger method="post" path="/register" baseUrl="https://nekoya.moe.team/api" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" required="true" name="email" %}
xxx@example.com
{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" required="true" %}
1 - 64 string characters
{% endswagger-parameter %}

{% swagger-parameter in="body" name="first_name" required="true" %}
First Name
{% endswagger-parameter %}

{% swagger-parameter in="body" name="last_name" required="true" %}
Last Name
{% endswagger-parameter %}

{% swagger-parameter in="header" required="true" name="Content-Type" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "message": "Register Verification Sent ~"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "message": "Bad Request"
}
```
{% endswagger-response %}
{% endswagger %}

## Login

{% swagger method="post" path="/login" baseUrl="https://nekoya.moe.team/api" summary="Account without 2FA Enabled" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="email" required="true" %}
xxx@example.com
{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" required="true" %}
1 - 64 string characters
{% endswagger-parameter %}

{% swagger-parameter in="body" name="ua" %}
User Agent
{% endswagger-parameter %}

{% swagger-parameter in="body" name="ip" %}
IP Address
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" required="true" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 29,
    "first_name": "Celia",
    "last_name": "Claire",
    "email": "celia@moe.team",
    "verify": true,
    "otp": false,
    "session_token": "2RBHSp3I8jjDzjuKaXXDWadJqRkJ1M3Q8nTmF9mioAL73OVZO8zc73sg4VBCVLQeXQRtbXZ6gQ5r1vjupkzoZP1HiRBXgHw74O7eKki6SPHIDYuxVfAdn6jPZ76HRRqI1jR1aKOdhwMq5RgOK7eMB5HEUKNu6gHIQkncoxRxz1eh5QGwGa9vYPW7TE3izEDbkGEqlIbnGf6O9foTty5HiJilPLtgVFvHUSoN6t7yDMXy2NjI0a4bKu5Pb6de0inh"
}
```
{% endswagger-response %}

{% swagger-response status="204: No Content" description="" %}
```javascript
{
    "message": "Sorry You haven't verified your email"
}
```
{% endswagger-response %}

{% swagger-response status="205: Reset Content" description="" %}
```javascript
{
    "message": "Sorry Your email is not registered in our system"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "message": "Bad Request"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "message": "Unauthorized"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/login" baseUrl="https://nekoya.moe.team/api" summary="Account with 2FA Enabled" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="email" required="true" %}
xxx@example.com
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" required="true" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" required="true" %}
1 - 64 string characters
{% endswagger-parameter %}

{% swagger-parameter in="body" name="ua" %}
User Agent
{% endswagger-parameter %}

{% swagger-parameter in="body" name="ip" %}
IP Address
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "message": "OTP Verification Sent ~",
    "otp": true,
    "token": "Xb5VNMMfoWZyHf22EMS3MjmgFdjDnAPTM3OoCh3CYP8sF6ospVzAaTjCPVM5FM5c"
}
```
{% endswagger-response %}

{% swagger-response status="204: No Content" description="" %}
```javascript
{
    "message": "Sorry You haven't verified your email"
}
```
{% endswagger-response %}

{% swagger-response status="205: Reset Content" description="" %}
```javascript
{
    "message": "Sorry Your email is not registered in our system"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "message": "Bad Request"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "message": "Unauthorized"
}
```
{% endswagger-response %}
{% endswagger %}

## OTP

{% swagger method="post" path="/otp-submit" baseUrl="https://nekoya.moe.team/api" summary="Submit OTP" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Content-Type" required="true" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-parameter in="body" name="token" required="true" %}
Encrypted String
{% endswagger-parameter %}

{% swagger-parameter in="body" name="code" required="true" type="" %}
OTP Code (6 digit)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "id": 29,
    "first_name": "Celia",
    "last_name": "Claire",
    "email": "celia@moe.team",
    "verify": true,
    "otp": true,
    "session_token": "2RBHSp3I8jjDzjuKaXXDWadJqRkJ1M3Q8nTmF9mioAL73OVZO8zc73sg4VBCVLQeXQRtbXZ6gQ5r1vjupkzoZP1HiRBXgHw74O7eKki6SPHIDYuxVfAdn6jPZ76HRRqI1jR1aKOdhwMq5RgOK7eMB5HEUKNu6gHIQkncoxRxz1eh5QGwGa9vYPW7TE3izEDbkGEqlIbnGf6O9foTty5HiJilPLtgVFvHUSoN6t7yDMXy2NjI0a4bKu5Pb6de0inh"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "message": "Bad Request"
}
```
{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}
```javascript
{
    "message": "Invalid OTP Code"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/otp-toggle" baseUrl="https://nekoya.moe.team/api" summary="Enable / Disable OTP" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="key" required="true" %}
Encrypted String
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" required="true" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "message": "Success set OTP to true",
    "otp": true
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "message": "Bad Request"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "message": "Unauthorized"
}
```
{% endswagger-response %}
{% endswagger %}

## Verify Account (Mail)

{% swagger method="post" path="/verify-mail" baseUrl="https://nekoya.moe.team/api" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="token" required="true" %}
Encrypted String
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" required="true" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "message": "Verified ~"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "message": "Bad Request"
}
```
{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}
```javascript
{
    "message": "Forbidden"
}
```
{% endswagger-response %}
{% endswagger %}

## Reset Password

{% swagger method="post" path="/request-reset-password" baseUrl="https://nekoya.moe.team/api" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="email" required="true" %}
xxx@example.com
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" required="true" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "message": "Reset Password Verification Sent ~"
}
```
{% endswagger-response %}

{% swagger-response status="205: Reset Content" description="" %}
```javascript
{
    "message": "Sorry Your email is not registered in our system"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "message": "Bad Request"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/reset-password" baseUrl="https://nekoya.moe.team/api" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="password" required="true" %}
1 - 64 string characters
{% endswagger-parameter %}

{% swagger-parameter in="query" name="token" required="true" %}
Encrypted String
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" required="true" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "message": "Success Reset Password ~"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "message": "Bad Request"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "message": "Unauthorized"
}
```
{% endswagger-response %}
{% endswagger %}

## Active Sessions

{% swagger method="post" path="/sessions" baseUrl="https://nekoya.moe.team/api" summary="Get All of Active Sessions" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="key" required="true" %}
Encrypted String
{% endswagger-parameter %}

{% swagger-parameter in="header" required="true" name="Content-Type" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
[
    {
        "user_agent": "Mozilla/5.0 (Linux; Android 12; M2012K11AG) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.41 Mobile Safari/537.36",
        "ip": "12.26.220.109",
        "session": "5ES9v6ekrGuuuKEDOpk2COGlmchHldplY10PnIIOuMUVpw32FsJy9aniQyX7RzeVan3muRWlKf02pWnIua127PKF0uPLxEccic8x5VFlN3OsyNFeJM8mdKAduRhwCIcID57vBanPrrYQ5vqv0FGbWcl29rtXk40YDUFvYoqy2VtBx5Us2sW1HYMT5EFrwC7H0T75kyRqL1ZmSJLMLKgPoUkhxOa1AMqqdy2dbSke8pOLQo20B7bgvEmxxyKcrV9C"
    }
]
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    "message": "Bad Request"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "message": "Unauthorized"
}
```
{% endswagger-response %}
{% endswagger %}
