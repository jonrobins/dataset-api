# Football Probabilities

#### \*\*\*\*

#### **Both Teams to Score \(BTTS\)** 

Based on PA’s extensive historical archive of historical results for the fixture, the probability of both teams scoring as expressed in percentage terms.  

**Over 2.5 Goals**

Based on PA’s extensive historical archive of historical results for the fixture, the probability of over 2.5 goals in the fixture expressed in percentage terms. 

**Match result**

Based on PA’s extensive historical archive of historical results for the fixture, the probabilities of various match results in the fixture, expressed in percentage terms broken down by home win, away win, or draw. 

**Match Scores**

Based on PA’s extensive historical archive of historical results for the fixture, the probabilities of various match scores in the fixture, expressed in percentage terms for each possible scoreline 

## **Schema**

{% tabs %}
{% tab title="Example" %}
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
{% endtab %}

{% tab title="Schema" %}
```javascript
{
    "$schema": "http://json-schema.org/draft-07/schema",
    "$id": "http://dataset.api.pamedia.io/football-predictions.json",
    "type": "object",
    "title": "The root schema",
    "description": "The root schema comprises the entire JSON document.",
    "required": [
        "id",
        "type",
        "name",
        "meta",
        "dataset"
    ],
    "properties": {
        "id": {
            "$id": "#/properties/id",
            "type": "string",
            "title": "The id schema",
            "description": "An explanation about the purpose of this instance."
        },
        "type": {
            "$id": "#/properties/type",
            "type": "string",
            "title": "The type schema",
            "description": "An explanation about the purpose of this instance."
        },
        "name": {
            "$id": "#/properties/name",
            "type": "string",
            "title": "The name schema",
            "description": "An explanation about the purpose of this instance."
        },
        "meta": {
            "$id": "#/properties/meta",
            "type": "object",
            "title": "The meta schema",
            "description": "An explanation about the purpose of this instance.",
            "required": [
                "matchId",
                "competition",
                "competitonId",
                "homeTeam",
                "homeTeamId",
                "awayTeam",
                "awayTeamId",
                "sport",
                "date"
            ],
            "properties": {
                "matchId": {
                    "$id": "#/properties/meta/properties/matchId",
                    "type": "string",
                    "title": "The matchId schema",
                    "description": "An explanation about the purpose of this instance."
                },
                "competition": {
                    "$id": "#/properties/meta/properties/competition",
                    "type": "string",
                    "title": "The competition schema",
                    "description": "An explanation about the purpose of this instance."
                },
                "competitonId": {
                    "$id": "#/properties/meta/properties/competitonId",
                    "type": "string",
                    "title": "The competitonId schema",
                    "description": "An explanation about the purpose of this instance."
                },
                "homeTeam": {
                    "$id": "#/properties/meta/properties/homeTeam",
                    "type": "string",
                    "title": "The homeTeam schema",
                    "description": "An explanation about the purpose of this instance."
                },
                "homeTeamId": {
                    "$id": "#/properties/meta/properties/homeTeamId",
                    "type": "string",
                    "title": "The homeTeamId schema",
                    "description": "An explanation about the purpose of this instance."
                },
                "awayTeam": {
                    "$id": "#/properties/meta/properties/awayTeam",
                    "type": "string",
                    "title": "The awayTeam schema",
                    "description": "An explanation about the purpose of this instance."
                },
                "awayTeamId": {
                    "$id": "#/properties/meta/properties/awayTeamId",
                    "type": "string",
                    "title": "The awayTeamId schema",
                    "description": "An explanation about the purpose of this instance."
                },
                "sport": {
                    "$id": "#/properties/meta/properties/sport",
                    "type": "string",
                    "title": "The sport schema",
                    "description": "An explanation about the purpose of this instance."
                },
                "date": {
                    "$id": "#/properties/meta/properties/date",
                    "type": "string",
                    "title": "The date schema",
                    "description": "An explanation about the purpose of this instance."
                }
            }
        },
        "dataset": {
            "$id": "#/properties/dataset",
            "type": "array",
            "title": "The dataset schema",
            "description": "An explanation about the purpose of this instance.",
            "additionalItems": true,
            "items": [
                {
                    "$id": "#/properties/dataset/items/0",
                    "type": "object",
                    "title": "The first items schema",
                    "description": "An explanation about the purpose of this instance.",
                    "required": [
                        "name",
                        "data"
                    ],
                    "properties": {
                        "name": {
                            "$id": "#/properties/dataset/items/0/properties/name",
                            "type": "string",
                            "title": "The name schema",
                            "description": "An explanation about the purpose of this instance."
                        },
                        "data": {
                            "$id": "#/properties/dataset/items/0/properties/data",
                            "type": "object",
                            "title": "The data schema",
                            "description": "An explanation about the purpose of this instance.",
                            "required": [
                                "home",
                                "away",
                                "draw"
                            ],
                            "properties": {
                                "home": {
                                    "$id": "#/properties/dataset/items/0/properties/data/properties/home",
                                    "type": "number",
                                    "title": "The home schema",
                                    "description": "An explanation about the purpose of this instance."
                                },
                                "away": {
                                    "$id": "#/properties/dataset/items/0/properties/data/properties/away",
                                    "type": "number",
                                    "title": "The away schema",
                                    "description": "An explanation about the purpose of this instance."
                                },
                                "draw": {
                                    "$id": "#/properties/dataset/items/0/properties/data/properties/draw",
                                    "type": "number",
                                    "title": "The draw schema",
                                    "description": "An explanation about the purpose of this instance."
                                }
                            }
                        }
                    }
                },
                {
                    "$id": "#/properties/dataset/items/1",
                    "type": "object",
                    "title": "The second items schema",
                    "description": "An explanation about the purpose of this instance.",
                    "required": [
                        "name",
                        "data"
                    ],
                    "properties": {
                        "name": {
                            "$id": "#/properties/dataset/items/1/properties/name",
                            "type": "string",
                            "title": "The name schema",
                            "description": "An explanation about the purpose of this instance."
                        },
                        "data": {
                            "$id": "#/properties/dataset/items/1/properties/data",
                            "type": "object",
                            "title": "The data schema",
                            "description": "An explanation about the purpose of this instance.",
                            "required": [
                                "scoreRatio"
                            ],
                            "properties": {
                                "scoreRatio": {
                                    "$id": "#/properties/dataset/items/1/properties/data/properties/scoreRatio",
                                    "type": "array",
                                    "title": "The scoreRatio schema",
                                    "description": "An explanation about the purpose of this instance.",
                                    "additionalItems": true,
                                    "items": {
                                        "$id": "#/properties/dataset/items/1/properties/data/properties/scoreRatio/items/0",
                                        "type": "object",
                                        "title": "The first items schema",
                                        "description": "An explanation about the purpose of this instance.",
                                        "required": [
                                            "home",
                                            "away",
                                            "value"
                                        ],
                                        "properties": {
                                            "home": {
                                                "$id": "#/properties/dataset/items/1/properties/data/properties/scoreRatio/items/0/properties/home",
                                                "type": "integer",
                                                "title": "The home schema",
                                                "description": "An explanation about the purpose of this instance."
                                            },
                                            "away": {
                                                "$id": "#/properties/dataset/items/1/properties/data/properties/scoreRatio/items/0/properties/away",
                                                "type": "integer",
                                                "title": "The away schema",
                                                "description": "An explanation about the purpose of this instance."
                                            },
                                            "value": {
                                                "$id": "#/properties/dataset/items/1/properties/data/properties/scoreRatio/items/0/properties/value",
                                                "type": "number",
                                                "title": "The value schema",
                                                "description": "An explanation about the purpose of this instance."
                                            }
                                        }
                                    }
                                }
                            }
                        }
                    }
                },
                {
                    "$id": "#/properties/dataset/items/2",
                    "type": "object",
                    "title": "The third items schema",
                    "description": "An explanation about the purpose of this instance.",
                    "required": [
                        "name",
                        "data"
                    ],
                    "properties": {
                        "name": {
                            "$id": "#/properties/dataset/items/2/properties/name",
                            "type": "string",
                            "title": "The name schema",
                            "description": "An explanation about the purpose of this instance."
                        },
                        "data": {
                            "$id": "#/properties/dataset/items/2/properties/data",
                            "type": "object",
                            "title": "The data schema",
                            "description": "An explanation about the purpose of this instance.",
                            "required": [
                                "over",
                                "under"
                            ],
                            "properties": {
                                "over": {
                                    "$id": "#/properties/dataset/items/2/properties/data/properties/over",
                                    "type": "number",
                                    "title": "The over schema",
                                    "description": "An explanation about the purpose of this instance."
                                },
                                "under": {
                                    "$id": "#/properties/dataset/items/2/properties/data/properties/under",
                                    "type": "number",
                                    "title": "The under schema",
                                    "description": "An explanation about the purpose of this instance."
                                }
                            }
                        }
                    }
                },
                {
                    "$id": "#/properties/dataset/items/3",
                    "type": "object",
                    "title": "The fourth items schema",
                    "description": "An explanation about the purpose of this instance.",
                    "required": [
                        "name",
                        "data"
                    ],
                    "properties": {
                        "name": {
                            "$id": "#/properties/dataset/items/3/properties/name",
                            "type": "string",
                            "title": "The name schema",
                            "description": "An explanation about the purpose of this instance."
                        },
                        "data": {
                            "$id": "#/properties/dataset/items/3/properties/data",
                            "type": "object",
                            "title": "The data schema",
                            "description": "An explanation about the purpose of this instance.",
                            "required": [
                                "chance"
                            ],
                            "properties": {
                                "chance": {
                                    "$id": "#/properties/dataset/items/3/properties/data/properties/chance",
                                    "type": "number",
                                    "title": "The chance schema",
                                    "description": "An explanation about the purpose of this instance."
                                }
                            }
                        }
                    }
                }
            ]
        }
    }
}
```
{% endtab %}
{% endtabs %}

