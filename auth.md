# Auth

## Auth (MIREA AUTH)

{% swagger baseUrl="https://kurator" method="post" path="/signin" summary="auth user in system" fullWidth="true" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="email" required="true" type="string" %}
user email
{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" required="true" type="string" %}
user password
{% endswagger-parameter %}

{% swagger-response status="200" description="user successfully auth" %}
```javascript
{
    "token"="user personal token"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Incorrect data" %}
```javascript
{
    "status_response": false,
    "description": "bad data"
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="server error" %}
```javascript
{
   "status_response": false,
   "description": "server error!"
}
```
{% endswagger-response %}
{% endswagger %}
