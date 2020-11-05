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
    "name": "Southampton vs Arsenal Match Probabilities",
    "timestamp": "2020-11-04T12:33:58+00:00",
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
    "dataset": {
      "football-match-results": {
        "code": "football:match-results",
		    "name": "Match Results",
		    "data": {
          "home": 38.3,
          "away": 35.8,
          "draw": 25.9
        }
      },
      "football-goals-scored": {
        "code": "football:goals-scored",
		    "name": "Goals Scored",
		    "data": {
          "scoreRatio": [{
              "home": "0",
              "away": "0",
              "value": 6.2
           },
           {
              "home": "1",
              "away": "0",
              "value": 6.2
           },
           {
              "home": "2",
              "away": "0",
              "value": 6.2
           },
           {
              "home": "3",
              "away": "0",
              "value": 6.2
           },
           {
              "home": "4",
              "away": "0",
              "value": 6.2
           },
           {
              "home": "5+",
              "away": "0",
              "value": 6.2
           }]
        }
      },
      "football-2.5-goals": {
        "code": "football:2.5-goals",
		    "name": "2.5 goals",
		    "data": {
            "over": 0.1,
            "under": 54.4
        }
      },
      "football-both-teams-to-score": {
        "code": "football:both-teams-to-score",
		    "name": "Both Teams to Score",
		    "data": {
            "chance": 58.3
        }
      },
      "football-key-stats": {
        "code": "football:key-stats",
		    "name": "Key Stats",
		    "data": {
          "insight": [{
              "title": "Both teams to score: yes",
              "statistics": [
                  "15 of Southampton's last 20 home league matches have seen both teams score",
                  "9 of Arsenal's last 14 away league matches have seen both teams score"
                ]
           },{
              "title": "Over 2.5 Goals",
              "statistics": [
                  "17 of Southampton's last 25 league matches have seen over 2.5 goals scored",
                  "4 of Arsenal's last 5 league matches have seen over 2.5 goals scored"
                ]
           }]
        }
      }
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



