# Nomenclatures

{% swagger baseUrl="https://my.opencomp.fr" path="/api/v1/towns.json?api_key=:api_key" method="get" summary="/towns.json" %}
{% swagger-description %}
Ce point d'accès vous permet de récupérer les villes.
{% endswagger-description %}

{% swagger-parameter in="query" name="api_key" type="string" %}
Votre clé d'API
{% endswagger-parameter %}

{% swagger-response status="200" description="Cake successfully retrieved." %}
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
{% endswagger-response %}
{% endswagger %}

