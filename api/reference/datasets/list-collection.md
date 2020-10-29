# List Collection

{% api-method method="get" host="https://dataset.api.pamedia.io" path="/v1/dataset" %}
{% api-method-summary %}
List Dataset Collection
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to retrieve a collection of datasets defined by your search query.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="apikey" type="string" required=true %}
Authentication via apikey to allow client to access datasets
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="full" type="boolean" required=false %}
Setting full to true returns back the full payload of the dataset, saving you from having to retrieve the dataset using the get detail endpoint.
{% endapi-method-parameter %}

{% api-method-parameter name="meta.matchId" type="string" %}
Filter the results by the match by passing the match id assocated with the dataset
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Datasets successfully returned.
{% endapi-method-response-example-description %}

```javascript
{
	"total": "400",
	"items": [{
		"id": "fbf025d3-0c34-4637-b5e0-231140931079",
		"type": "sport:football:probabilities",
		"name": "Southampton vs Arsenal Match Predictions",
		"meta": {
			"matchId": "166273",
			"competition": "Premier League 2020",
			"competitonId": "71",
			"homeTeam": "Southampton",
			"homeTeamId": "54",
			"awayTeam": "Arsenal",
			"awayTeamId": "7",
			"sport": "Football",
			"date": "2020-03-01"
		}
	}, {
		"id": "64b42d7b-f1b8-4828-8b04-1af2b7a7951b",
		"type": "sport:football:probabilities",
		"name": "Southampton vs Manchester United Match Predictions",
		"meta": {
			"matchId": "352411",
			"competition": "Premier League 2020",
			"competitonId": "71",
			"homeTeam": "Southampton",
			"homeTeamId": "54",
			"awayTeam": "Manchester United",
			"awayTeamId": "17",
			"sport": "Football",
			"date": "2020-03-07"
		}
	}]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://dataset.api.pamedia.io" path="/v1/dataset?meta.matchId=166273&full=true" %}
{% api-method-summary %}
List Dataset Collection with Full Query Parameter Set 
{% endapi-method-summary %}

{% api-method-description %}
This endpoint demonstrates what the payload looks like when the full query parameter is set, this will provide you with an example of how the payloads differs.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="meta.matchId" type="string" required=true %}
Example Match ID
{% endapi-method-parameter %}

{% api-method-parameter name="full" type="boolean" required=true %}
Full set to true
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
	"total": "1",
	"items": [{
		"id": "fbf025d3-0c34-4637-b5e0-231140931079",
		"type": "sport:football:probabilities",
		"name": "Southampton vs Arsenal Match Predictions",
		"meta": {
			"matchId": "166273",
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
	}]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

