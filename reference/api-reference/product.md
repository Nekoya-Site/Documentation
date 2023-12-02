# Product

## All Products

{% swagger method="get" path="/getproducts" baseUrl="https://nekoya.moe.team/api" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
```javascript
[
  {
    "ID": "306796_02",
    "TITLE": "Scuderia Ferrari Speedcat Men's Motorsport Shoes",
    "IMAGE": "Product_18.webp",
    "DESCRIPTION": "Born for speed. Raised in style. The Speedcat returns over 20 years later, this time with sleek Scuderia Ferrari engineering. The signature low profile silhouette features a premium suede upper, plus an authentic rounded driver's heel and Scuderia Ferrari racing shield at the heel. Taking iconic track style to the streets.",
    "STOCK": 99,
    "PRICE": 1500000,
    "SIZE": "46",
    "DISCOUNT": 0,
    "BRAND": "Puma"
  },
  {
    "ID": "306807_01",
    "TITLE": "Ferrari Nitefox GT Men's Shoes",
    "IMAGE": "Product_20.webp",
    "DESCRIPTION": "In Partnership with Scuderia Ferrari, the Nitefox GT is inspired by the Ferrari Testarossa’s aerodynamics. One of the most iconic elements is the wind takes on side of the car, giving a very distinctive look.",
    "STOCK": 99,
    "PRICE": 4500000,
    "SIZE": "47",
    "DISCOUNT": 20,
    "BRAND": "Puma"
  },
  {
    "ID": "306809_03",
    "TITLE": "Scuderia Ferrari RCT XETIC Forza Men's ",
    "IMAGE": "Product_19.webp",
    "DESCRIPTION": "This progressive motorsport silhouette uses ground-breaking XETIC cushioning technology to bring you a sleek, high-tech shoe with an ultimately shock-absorbing stride. With sleek Ferrari branding and team colors, it's built for life in the fast lane.",
    "STOCK": 99,
    "PRICE": 2200000,
    "SIZE": "45",
    "DISCOUNT": 0,
    "BRAND": "Puma"
  },
  {
    "ID": "306842_02",
    "TITLE": "Mercedes F1 RS Connect Motorsport Shoes",
    "IMAGE": "Product_17.webp",
    "DESCRIPTION": "This innovative addition to the Running System family is inspired by the revolution in connection and communication in our modern, digital world. The RS Connect rides the wave of technological transformation, with a fresh, futuristic design in eye-popping monochrome neon. A richly layered upper and premium Mercedes-AMG Petronas Motorsport branding at the heel bring a high-end, motorsport feel to these comfortable, cushioned sneaks.",
    "STOCK": 99,
    "PRICE": 2000000,
    "SIZE": "47",
    "DISCOUNT": 0,
    "BRAND": "Puma"
  }
]
```
{% endswagger-response %}
{% endswagger %}

## Product Info

{% swagger method="get" path="/getproduct" baseUrl="https://nekoya.moe.team/api" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="id" required="true" %}
Product ID
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
[
  {
    "ID": "GY8803",
    "TITLE": "Nano X1 Men's Training Shoes",
    "IMAGE": "Product_37.webp",
    "DESCRIPTION": "Climb, jump and throw the barbell around in shoes made for the way you work out. Perfected by elite athletes, Reebok Nano X1 Shoes are made for anyone who loves to train hard. This men's version has a Flexweave® knit upper that's breathable yet durable, with integrated support for multidirectional movement. Floatride Energy Foam cushioning in the forefoot provides a responsive feel. A heel clip adds stability.",
    "STOCK": 99,
    "PRICE": 1800000,
    "SIZE": "45",
    "DISCOUNT": 0,
    "BRAND": "Reebok"
  }
]
```
{% endswagger-response %}
{% endswagger %}
