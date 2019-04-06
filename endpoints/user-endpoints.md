---
description: All user endpoints
---

# User endpoints

{% api-method method="get" host="https://api.hawkbot.cc" path="/user/:id" %}
{% api-method-summary %}
Get user
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="User id" type="integer" required=true %}
The ID of the user you are looking for
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
When the user you was looking for exists
{% endapi-method-response-example-description %}

```
{
  "languageTag": "en-US",
  "id": "416902379598774273"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
When you provided an invalid id
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
When there was no user with the provided id
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



