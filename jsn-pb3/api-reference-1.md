# API Reference

{% api-method method="get" host="https://your-joomla-site.com" path="/index.php?option=com\_ajax&plugin=pagebuilder3&format=json&task=getElements" %}
{% api-method-summary %}
Get Elements
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="task" type="string" required=true %}
getElements
{% endapi-method-parameter %}

{% api-method-parameter name="format" type="string" required=false %}
json
{% endapi-method-parameter %}

{% api-method-parameter name="plugin" type="string" required=true %}
pagebuilder3
{% endapi-method-parameter %}

{% api-method-parameter name="option" type="string" required=true %}
com\_ajax
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "name": "Cake's name",
    "recipe": "Cake's recipe name",
    "cake": "Binary cake"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Ain't no cake like that."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



{% api-method method="post" host="https://your-joomla-site.com" path="/index.php?option=com\_ajax&plugin=pagebuilder3&format=json&task=saveElement" %}
{% api-method-summary %}
Save Element
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="task" type="string" required=true %}
saveElement
{% endapi-method-parameter %}

{% api-method-parameter name="format" type="string" required=false %}
json
{% endapi-method-parameter %}

{% api-method-parameter name="plugin" type="string" required=true %}
pagebuilder3
{% endapi-method-parameter %}

{% api-method-parameter name="option" type="string" required=true %}
com\_ajax
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="status" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="html" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="data" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="element\_id" type="string" required=false %}
For Update the element
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



{% api-method method="post" host="https://your-joomla-site.com" path="/index.php?option=com\_ajax&plugin=pagebuilder3&format=json&task=deleteElement" %}
{% api-method-summary %}
Delete Element
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="task" type="string" required=true %}
getElements
{% endapi-method-parameter %}

{% api-method-parameter name="format" type="string" required=false %}
json
{% endapi-method-parameter %}

{% api-method-parameter name="plugin" type="string" required=true %}
pagebuilder3
{% endapi-method-parameter %}

{% api-method-parameter name="option" type="string" required=true %}
com\_ajax
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="element\_id" type="string" required=false %}
ID of element to delete
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "name": "Cake's name",
    "recipe": "Cake's recipe name",
    "cake": "Binary cake"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Ain't no cake like that."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



