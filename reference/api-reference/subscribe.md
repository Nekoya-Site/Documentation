# Subscribe

{% swagger method="get" path="/subscribe" baseUrl="https://nekoya.moe.team/api" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="email" required="true" %}
xxx@example.com
{% endswagger-parameter %}

{% swagger-response status="201: Created" description="" %}
```javascript
{
    "message": "Success"
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
