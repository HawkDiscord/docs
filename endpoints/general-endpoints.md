---
description: A list of endpoints which doesn't belong to an explicit group
---

# General endpoints

{% api-method method="get" host="https://api.hawkbot.cc" path="/" %}
{% api-method-summary %}
Get information
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get an general overview of the API
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Information when your request got processed
{% endapi-method-response-example-description %}

```javascript
{
  "version": "1.0",
  "github": "https://github.com/DRSchlaubi/regnum",
  "docs": "http://docs.hawkbot.cc"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.hawkbot.cc" path="/docs" %}
{% api-method-summary %}
Get docs
{% endapi-method-summary %}

{% api-method-description %}
Returns an 301 redirect to this page
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns an 301 redirect to this page
{% endapi-method-response-example-description %}

```
301 https://docs.hawkbot.cc
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.hawkbot.cc" path="/metrics" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}
Returns some basic metrics about the bot
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns a metrics object
{% endapi-method-response-example-description %}

```
{
  "@class": "cc.hawkbot.regnum.entites.packets.MetricsPacket",
  "discordRestPing": 148,
  "discordGatewayPing": 132,
  "usedMemory": 3963196992,
  "availableMemory": 4183818240,
  "cpuUsage": 12,
  "cpus": 12,
  "guilds": 2,
  "users": 21
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

