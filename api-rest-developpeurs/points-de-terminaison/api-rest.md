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
    "id": 17,
    "title": "CE1\/CE2",
    "year_id": 5,
    "establishment_id": "DEMO",
    "created": "2015-09-08T00:00:00+0000",
    "pupils": [
        {
            "id": 128,
            "name": "Bailly",
            "first_name": "Rom\u00e9o",
            "sex": "F",
            "birthday": "2008-01-27T00:00:00+0000",
            "state": null,
            "tutor_id": null,
            "created": "2015-09-08T00:00:00+0000",
            "levels": [
                {
                    "id": 1123,
                    "title": "CE2",
                    "cycle_id": 2,
                    "_joinData": {
                        "level_id": 1123,
                        "id": 164,
                        "classroom_id": 17,
                        "pupil_id": 128
                    }
                }
            ],
            "_joinData": {
                "pupil_id": 128,
                "id": 164,
                "classroom_id": 17,
                "level_id": 1123
            }
        },
        {
            "id": 129,
            "name": "Simon",
            "first_name": "Constant",
            "sex": "M",
            "birthday": "2008-11-21T00:00:00+0000",
            "state": null,
            "tutor_id": null,
            "created": "2015-09-08T00:00:00+0000",
            "levels": [
                {
                    "id": 1123,
                    "title": "CE2",
                    "cycle_id": 2,
                    "_joinData": {
                        "level_id": 1123,
                        "id": 165,
                        "classroom_id": 17,
                        "pupil_id": 129
                    }
                }
            ],
            "_joinData": {
                "pupil_id": 129,
                "id": 165,
                "classroom_id": 17,
                "level_id": 1123
            }
        },
        {
            "id": 130,
            "name": "Cordier",
            "first_name": "Ma\u00eblle",
            "sex": "M",
            "birthday": "2008-07-18T00:00:00+0000",
            "state": null,
            "tutor_id": null,
            "created": "2015-09-08T00:00:00+0000",
            "levels": [
                {
                    "id": 1123,
                    "title": "CE2",
                    "cycle_id": 2,
                    "_joinData": {
                        "level_id": 1123,
                        "id": 166,
                        "classroom_id": 17,
                        "pupil_id": 130
                    }
                }
            ],
            "_joinData": {
                "pupil_id": 130,
                "id": 166,
                "classroom_id": 17,
                "level_id": 1123
            }
        }
    ],
    "year": {
        "id": 5,
        "title": "2015\/2016"
    },
    "establishment": {
        "id": "DEMO",
        "name": "\u00c9tablissement de d\u00e9monstration",
        "main_naming": null,
        "uai_patronym": null,
        "sector": "Public",
        "address": "21 rue des Lilas",
        "town_id": "80164",
        "locality": null,
        "X": null,
        "Y": null,
        "user_id": 1
    }
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



