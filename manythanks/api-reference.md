# API Reference

{% api-method method="get" host="https://manythanks.pagefly.io" path="/api/shopify/thankyou" %}
{% api-method-summary %}
Get thank you page data
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get the shop's thank you page data
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Page successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "data": {
        "createdAt": "2018-04-23T08:08:48.123Z", // ISO Datetime
        "updatedAt": "2018-04-23T05:37:31.798Z",
        "_id": "5add707ebe7ba17e39453470", // Mongo ObjectID(),
        "shopDomain": "minhpt.myshopify.com",
        "status": "published", // published or not
        "configs": {},
        "metadata": {},
        "html": "11111111111",
        "data": {},
        "type": "thankyou"
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a page matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "success": false,
    "errors": {}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://manythanks.pagefly.io" path="/api/shopify/thankyou" %}
{% api-method-summary %}
Create/Update thank you page
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="html" type="object" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="data" type="object" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="metadata" type="object" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="configs" type="object" required=false %}

{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "errors": null,
    "data": {
        "n": 1,
        "nModified": 1,
        "ok": 1
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



