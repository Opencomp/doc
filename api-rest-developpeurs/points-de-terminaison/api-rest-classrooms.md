# Classes

{% api-method method="get" host="https://my.opencomp.fr" path="/api/v1/classrooms/:id.:format?api\_key=:api\_key" %}
{% api-method-summary %}
/classrooms/:id.json
{% endapi-method-summary %}

{% api-method-description %}
Ce point d'accès vous permet de récupérer une classe.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
L'identifiant de la classe à récupérer.
{% endapi-method-parameter %}

{% api-method-parameter name="format" type="string" required=true %}
Le format de données à récupérer en sortie.  
Peut être **`json`** ou **`xml`**.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="api\_key" type="string" required=true %}
Votre clé d'API.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Classe récupérée avec succès
{% endapi-method-response-example-description %}

```javascript
{
    "id": 109,
    "id_be": 10001455,
    "title": "Classe de d\u00e9mo 2018",
    "year_id": 8,
    "establishment_id": "DEMO1234",
    "created": "2018-08-14T00:00:00+00:00",
    "pupils_count": 25,
    "evaluations_count": 4,
    "license_key": null
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
La clé d'API est manquante ou n'existe pas.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "API Key is missing or invalid. Retry with api_key query parameter.",
    "url": "\/api\/v1\/classrooms\/view\/17.json",
    "code": 401
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
La clé d'API est valide mais vous n'avez pas la permission d'accéder à la ressource demandée.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Vous n\u0027\u00eates pas autoris\u00e9 \u00e0 acc\u00e9der \u00e0 cet emplacement.",
    "url": "\/api\/v1\/classrooms\/view\/17.json?api_key=cc9e40009-5644-11e6-bec8-0242ac120004",
    "code": 403
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



