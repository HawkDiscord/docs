---
description: All guild endpoints
---

# Guild endpoints

{% api-method method="get" host="https://api.hawkbot.cc" path="/guilds/:id" %}
{% api-method-summary %}
Get guild
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
The ID of the guild you are lookking for
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Guild successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
  "prefix": "%NO%",
  "blacklistedChannels": [
    547841578664984586
  ],
  "whitelistedChannels": null,
  "languageTag": "en-US",
  "id": "546603778590375947"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
When the provided id was invalid
{% endapi-method-response-example-description %}

```
{
  "code": 400,
  "message": "Bad request",
  "description": "Invalid id provided"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
When there was no guild with the specified ID
{% endapi-method-response-example-description %}

```
{
  "code": 404,
  "message": "Not found",
  "description": "Entity not found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



