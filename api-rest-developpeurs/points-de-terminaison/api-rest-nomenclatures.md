# Nomenclatures

{% api-method method="get" host="https://my.opencomp.fr" path="/api/v1/towns.json?api\_key=:api\_key" %}
{% api-method-summary %}
/towns.json
{% endapi-method-summary %}

{% api-method-description %}
Ce point d'accès vous permet de récupérer les villes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="api\_key" type="string" required=true %}
Votre clé d'API
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
    "items": [
        {
            "id": "02013",
            "name": "Amifontaine",
            "academy_id": 20,
            "academy": {
                "id": 20,
                "name": "Amiens"
            }
        },
        {
            "id": "02014",
            "name": "Amigny-Rouy",
            "academy_id": 20,
            "academy": {
                "id": 20,
                "name": "Amiens"
            }
        },
        {
            "id": "06002",
            "name": "Amirat",
            "academy_id": 23,
            "academy": {
                "id": 23,
                "name": "Nice"
            }
        },
        {
            "id": "28006",
            "name": "Amilly",
            "academy_id": 18,
            "academy": {
                "id": 18,
                "name": "Orl\u00e9ans-Tours"
            }
        },
        {
            "id": "42004",
            "name": "Amions",
            "academy_id": 10,
            "academy": {
                "id": 10,
                "name": "Lyon"
            }
        },
        {
            "id": "45004",
            "name": "Amilly",
            "academy_id": 18,
            "academy": {
                "id": 18,
                "name": "Orl\u00e9ans-Tours"
            }
        },
        {
            "id": "50006",
            "name": "Amigny",
            "academy_id": 5,
            "academy": {
                "id": 5,
                "name": "Caen"
            }
        },
        {
            "id": "77002",
            "name": "Amillis",
            "academy_id": 24,
            "academy": {
                "id": 24,
                "name": "Cr\u00e9teil"
            }
        },
        {
            "id": "80021",
            "name": "Amiens",
            "academy_id": 20,
            "academy": {
                "id": 20,
                "name": "Amiens"
            }
        }
    ],
    "total_count": 9
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



