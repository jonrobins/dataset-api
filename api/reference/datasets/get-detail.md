# Get Detail

{% api-method method="get" host="https://dataset.api.pamedia.io" path="/v1/dataset/:id" %}
{% api-method-summary %}
Get Dataset
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to the dataset via its id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
ID of the dataset to retrieve
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="apikey" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "id": "fbf025d3-0c34-4637-b5e0-231140931079",
    "type": "sport:football:probabilities",
    "name": "Southampton vs Arsenal Match Predictions",
    "meta": {
        "matchId": "123441",
        "competition": "Premier League 2020",
        "competitonId": "71",
        "homeTeam": "Southampton",
        "homeTeamId": "54",
        "awayTeam": "Arsenal",
        "awayTeamId": "7",
        "sport": "Football",
        "date": "2020-03-01"
    },
    "dataset": [{
        "name": "football:match-results",
        "data": {
            "home": 38.3,
            "away": 35.8,
            "draw": 25.9
        }
    }, {
        "name": "football:goals-scored",
        "data": {
            "scoreRatio": [{
                "home": 0,
                "away": 0,
                "value": 6.2
            }]
        }
    }, {
        "name": "football:2.5-goals",
        "data": {
            "over": 0.1,
            "under": 54.4
        }
    }, {
        "name": "football:both-teams-to-score",
        "data": {
            "chance": 58.3
        }
    }]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



