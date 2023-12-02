# Transaction

## Create Transaction

{% swagger method="post" path="/checkout" baseUrl="https://nekoya.moe.team/api" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="firstName" required="true" %}
First Name
{% endswagger-parameter %}

{% swagger-parameter in="query" name="key" required="true" %}
Encrypted String
{% endswagger-parameter %}

{% swagger-parameter in="body" name="lastName" required="true" %}
Last Name
{% endswagger-parameter %}

{% swagger-parameter in="body" name="phoneNumber" required="true" %}
(+1) xxx xxx xxx
{% endswagger-parameter %}

{% swagger-parameter in="body" name="streetAddress1" required="true" %}
Street Address
{% endswagger-parameter %}

{% swagger-parameter in="body" name="streetAddress2" required="true" %}
Street Addres (Alternative)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="region" required="true" %}
Region
{% endswagger-parameter %}

{% swagger-parameter in="body" name="province" required="true" %}
Province
{% endswagger-parameter %}

{% swagger-parameter in="body" name="city" required="true" %}
City
{% endswagger-parameter %}

{% swagger-parameter in="body" name="district" required="true" %}
District
{% endswagger-parameter %}

{% swagger-parameter in="body" name="subDistrict" required="true" %}
Sub District
{% endswagger-parameter %}

{% swagger-parameter in="body" name="postalCode" required="true" %}
Postal Code
{% endswagger-parameter %}

{% swagger-parameter in="body" name="logistic" required="true" %}
Logistic Provider (JNE, JNT, SICEPAT)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="data" required="true" type="String (JSON)" %}
Order Data
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-response status="201: Created" description="" %}
```javascript
{
    "order_id": 3,
    "data": "{'product_id': '306796_02', 'quantity': 35}"
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

## All Transactions

{% swagger method="post" path="/transaction" baseUrl="https://nekoya.moe.team/api" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="key" required="true" %}
Encrypted String
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Content-Type" %}
application/x-www-form-urlencoded
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
[
    {
        "id": 1,
        "userId": 14,
        "firstName": "Gawr",
        "lastName": "Gura",
        "phoneNumber": "081238749274",
        "streetAddress1": "Isekai",
        "streetAddress2": "Isekai 2",
        "region": "Indonesia",
        "province": "DKI Jakarta",
        "city": "Jakarta",
        "district": "Jakarta Utara",
        "subDistrict": "Penjaringan",
        "postalCode": "11330",
        "logistic": "JNE",
        "paymentMethod": "-",
        "data": "[\n  {\n    \"product_id\": \"306796_02\",\n    \"quantity\": 30\n  }\n]",
        "paid": "0",
        "status": "pending"
    },
    {
        "id": 2,
        "userId": 14,
        "firstName": "Minato",
        "lastName": "Aqua",
        "phoneNumber": "081238749274",
        "streetAddress1": "Isekai",
        "streetAddress2": "Isekai 2",
        "region": "Indonesia",
        "province": "DKI Jakarta",
        "city": "Jakarta",
        "district": "Jakarta Utara",
        "subDistrict": "Penjaringan",
        "postalCode": "11330",
        "logistic": "JNE",
        "paymentMethod": "-",
        "data": "[{\"product_id\": \"306796_02\",\"quantity\": 35}]",
        "paid": "0",
        "status": "pending"
    },
    {
        "id": 3,
        "userId": 14,
        "firstName": "Akai",
        "lastName": "Haato",
        "phoneNumber": "081238749274",
        "streetAddress1": "Isekai",
        "streetAddress2": "Isekai 2",
        "region": "Indonesia",
        "province": "DKI Jakarta",
        "city": "Jakarta",
        "district": "Jakarta Utara",
        "subDistrict": "Penjaringan",
        "postalCode": "11330",
        "logistic": "JNE",
        "paymentMethod": "-",
        "data": "[{\"product_id\": \"306796_02\",\"quantity\": 35}]",
        "paid": "0",
        "status": "pending"
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
