# Classes

{% swagger baseUrl="https://my.opencomp.fr" path="/api/v1/classrooms/:id.:format?api_key=:api_key" method="get" summary="/classrooms/:id.json" %}
{% swagger-description %}
Ce point d'accès vous permet de récupérer une classe.
{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="integer" %}
L'identifiant de la classe à récupérer.
{% endswagger-parameter %}

{% swagger-parameter in="path" name="format" type="string" %}
Le format de données à récupérer en sortie.

\


Peut être 

**`json`**

 ou 

**`xml`**

.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="api_key" type="string" %}
Votre clé d'API.
{% endswagger-parameter %}

{% swagger-response status="200" description="Classe récupérée avec succès" %}
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
{% endswagger-response %}

{% swagger-response status="401" description="La clé d'API est manquante ou n'existe pas." %}
```javascript
{
    "message": "API Key is missing or invalid. Retry with api_key query parameter.",
    "url": "\/api\/v1\/classrooms\/view\/17.json",
    "code": 401
}
```
{% endswagger-response %}

{% swagger-response status="403" description="La clé d'API est valide mais vous n'avez pas la permission d'accéder à la ressource demandée." %}
```javascript
{
    "message": "Vous n\u0027\u00eates pas autoris\u00e9 \u00e0 acc\u00e9der \u00e0 cet emplacement.",
    "url": "\/api\/v1\/classrooms\/view\/17.json?api_key=cc9e40009-5644-11e6-bec8-0242ac120004",
    "code": 403
}
```
{% endswagger-response %}
{% endswagger %}

