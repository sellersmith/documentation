# API Reference

## 

## PageFly Elements API

{% api-method method="get" host="https://apps.pagefly.io" path="/index.php?task=elements&id=${shop\_id}" %}
{% api-method-summary %}
Get Elements
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get list of saved elements.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="id" type="number" required=true %}
Shop ID that get from `window.pagefly_data.shopify_id`
{% endapi-method-parameter %}

{% api-method-parameter name="task" type="string" required=true %}
`task=elements`
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Elements successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "data": [
        {
            id: 123,
            data: 'Element JSON data',
            html: 'Element HTML data',
            type: 'Element type',
            status: 'Status of the element'
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://apps.pagefly.io" path="/index.php?task=elements&id=${shop\_id}&type=SAVE" %}
{% api-method-summary %}
Save Element
{% endapi-method-summary %}

{% api-method-description %}
Save Element to database
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="type" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="task" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="id" type="number" required=true %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="type" type="string" required=false %}
Element type
{% endapi-method-parameter %}

{% api-method-parameter name="html" type="string" required=false %}
Element HTML
{% endapi-method-parameter %}

{% api-method-parameter name="data" type="string" required=true %}
Element JSON data
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://apps.pagefly.io" path="/index.php?task=elements&id=${shop\_id}&type=DELETE&element\_id=${element\_id}" %}
{% api-method-summary %}
Delete Element
{% endapi-method-summary %}

{% api-method-description %}
Delete element by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="element\_id" type="string" required=true %}
Element ID
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://apps.pagefly.io" path="/index.php?task=elements&id=${shop\_id}&type=SAVE" %}
{% api-method-summary %}
Update Element
{% endapi-method-summary %}

{% api-method-description %}
Update Element
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="type" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="task" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="id" type="number" required=true %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="element\_id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=false %}
Element type
{% endapi-method-parameter %}

{% api-method-parameter name="html" type="string" required=false %}
Element HTML
{% endapi-method-parameter %}

{% api-method-parameter name="data" type="string" required=true %}
Element JSON data
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://media.pagefly.io" path="/file/delete/:id" %}
{% api-method-summary %}
Delete Image
{% endapi-method-summary %}

{% api-method-description %}
Delete image by the id of image.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Image ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="password" type="string" required=false %}
123
{% endapi-method-parameter %}

{% api-method-parameter name="username" type="string" required=false %}
minh
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Revision API



