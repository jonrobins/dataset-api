# Football Probabilities

This section of the documentation provides a breakdown of our coverage for football probabilities and analytical insights. Please see below the various field descriptions along with examples on how you can expect to call and see this data presented. 

Using our Football API \(link to docs\) match ID, these fields can be used to compliment our football data coverage.

#### **Both Teams to Score \(BTTS\)** 

Based on PA’s extensive historical archive of historical results for the fixture, the probability of both teams scoring as expressed in percentage terms.  

**Over 2.5 Goals**

Based on PA’s extensive historical archive of historical results for the fixture, the probability of over 2.5 goals in the fixture expressed in percentage terms. 

**Match result**

Based on PA’s extensive historical archive of historical results for the fixture, the probabilities of various match results in the fixture, expressed in percentage terms broken down by home win, away win, or draw. 

**Match Scores**

Based on PA’s extensive historical archive of historical results for the fixture, the probabilities of various match scores in the fixture, expressed in percentage terms for each possible scoreline 

## **Data Schema & Examples**

{% tabs %}
{% tab title="Example" %}
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
{% endtab %}

{% tab title="Schema" %}
```javascript
{
    "$schema": "http://json-schema.org/draft-07/schema",
    "$id": "http://dataset.pamedia.io/dataset.json",
    "type": "object",
    "required": ["id", "type", "name", "timestamp", "meta", "dataset"],
    "properties": {
        "id": {
            "$id": "#/properties/id",
            "type": "string"
        },
        "type": {
            "$id": "#/properties/type",
            "type": "string"
        },
        "name": {
            "$id": "#/properties/name",
            "type": "string"
        },
        "timestamp": {
            "$id": "#/properties/timestamp",
            "type": "string"
        },
        "meta": {
            "$id": "#/properties/meta",
            "type": "object",
            "required": [],
            "properties": {
                "matchId": {
                    "$id": "#/properties/meta/properties/matchId",
                    "type": "string"
                },
                "competition": {
                    "$id": "#/properties/meta/properties/competition",
                    "type": "string"
                },
                "competitonId": {
                    "$id": "#/properties/meta/properties/competitonId",
                    "type": "string"
                },
                "homeTeam": {
                    "$id": "#/properties/meta/properties/homeTeam",
                    "type": "string"
                },
                "homeTeamId": {
                    "$id": "#/properties/meta/properties/homeTeamId",
                    "type": "string"
                },
                "awayTeam": {
                    "$id": "#/properties/meta/properties/awayTeam",
                    "type": "string"
                },
                "awayTeamId": {
                    "$id": "#/properties/meta/properties/awayTeamId",
                    "type": "string"
                },
                "sport": {
                    "$id": "#/properties/meta/properties/sport",
                    "type": "string"
                },
                "date": {
                    "$id": "#/properties/meta/properties/date",
                    "type": "string"
                }
            }            
        },
        "dataset": {
            "$id": "#/properties/dataset",
            "type": "object",
            "required": [],
            "properties": {
                "football-match-results": {
                    "$id": "#/properties/dataset/properties/football-match-results",
                    "type": "object",
                    "required": ["code", "name", "data"],
                    "properties": {
                        "code": {
                            "$id": "#/properties/dataset/properties/football-match-results/properties/code",
                            "type": "string"
                        },
                        "name": {
                            "$id": "#/properties/dataset/properties/football-match-results/properties/name",
                            "type": "string"
                        },
                        "data": {
                            "$id": "#/properties/dataset/properties/football-match-results/properties/data",
                            "type": "object",
                            "required": ["home", "away", "draw"],
                            "properties": {
                                "home": {
                                    "$id": "#/properties/dataset/properties/football-match-results/properties/data/properties/home",
                                    "type": "number"
                                },
                                "away": {
                                    "$id": "#/properties/dataset/properties/football-match-results/properties/data/properties/away",
                                    "type": "number"
                                },
                                "draw": {
                                    "$id": "#/properties/dataset/properties/football-match-results/properties/data/properties/draw",
                                    "type": "number"
                                }
                            }                            
                        }
                    }
                },
                "football-goals-scored": {
                    "$id": "#/properties/dataset/properties/football-goals-scored",
                    "type": "object",
                    "required": ["code", "name", "data"],
                    "properties": {
                        "code": {
                            "$id": "#/properties/dataset/properties/football-goals-scored/properties/code",
                            "type": "string"
                        },
                        "name": {
                            "$id": "#/properties/dataset/properties/football-goals-scored/properties/name",
                            "type": "string"
                        },
                        "data": {
                            "$id": "#/properties/dataset/properties/football-goals-scored/properties/data",
                            "type": "object",
                            "required": ["scoreRatio"],
                            "properties": {
                                "scoreRatio": {
                                    "$id": "#/properties/dataset/properties/football-goals-scored/properties/data/properties/scoreRatio",
                                    "type": "array",
                                    "additionalItems": true,
                                    "items": {
                                        "$id": "#/properties/dataset/properties/football-goals-scored/properties/data/properties/scoreRatio/items",
                                        "type": "object",
                                        "required": ["home", "away", "value"],
                                        "properties": {
                                            "home": {
                                                "$id": "#/properties/dataset/properties/football-goals-scored/properties/data/properties/scoreRatio/items/properties/home",
                                                "type": "string"
                                            },
                                            "away": {
                                                "$id": "#/properties/dataset/properties/football-goals-scored/properties/data/properties/scoreRatio/items/properties/away",
                                                "type": "string"
                                            },
                                            "value": {
                                                "$id": "#/properties/dataset/properties/football-goals-scored/properties/data/properties/scoreRatio/items/properties/value",
                                                "type": "number"
                                            }
                                        }                                        
                                    }
                                }
                            }                            
                        }
                    }                    
                },
                "football-2.5-goals": {
                    "$id": "#/properties/dataset/properties/football-2.5-goals",
                    "type": "object",
                    "required": ["code", "name", "data"],
                    "properties": {
                        "code": {
                            "$id": "#/properties/dataset/properties/football-2.5-goals/properties/code",
                            "type": "string"
                        },
                        "name": {
                            "$id": "#/properties/dataset/properties/football-2.5-goals/properties/name",
                            "type": "string"
                        },
                        "data": {
                            "$id": "#/properties/dataset/properties/football-2.5-goals/properties/data",
                            "type": "object",
                            "required": ["over", "under"],
                            "properties": {
                                "over": {
                                    "$id": "#/properties/dataset/properties/football-2.5-goals/properties/data/properties/over",
                                    "type": "number"
                                },
                                "under": {
                                    "$id": "#/properties/dataset/properties/football-2.5-goals/properties/data/properties/under",
                                    "type": "number"
                                }
                            }
                        }
                    }                    
                },
                "football-both-teams-to-score": {
                    "$id": "#/properties/dataset/properties/football-both-teams-to-score",
                    "type": "object",
                    "required": ["code", "name", "data"],
                    "properties": {
                        "code": {
                            "$id": "#/properties/dataset/properties/football-both-teams-to-score/properties/code",
                            "type": "string"
                        },
                        "name": {
                            "$id": "#/properties/dataset/properties/football-both-teams-to-score/properties/name",
                            "type": "string"
                        },
                        "data": {
                            "$id": "#/properties/dataset/properties/football-both-teams-to-score/properties/data",
                            "type": "object",
                            "required": ["chance"],
                            "properties": {
                                "chance": {
                                    "$id": "#/properties/dataset/properties/football-both-teams-to-score/properties/data/properties/chance",
                                    "type": "number"
                                }
                            }                            
                        }
                    }                    
                },
                "football-key-stats": {
                    "$id": "#/properties/dataset/properties/football-key-stats",
                    "type": "object",
                    "required": ["code", "name", "data"],
                    "properties": {
                        "code": {
                            "$id": "#/properties/dataset/properties/football-key-stats/properties/code",
                            "type": "string"
                        },
                        "name": {
                            "$id": "#/properties/dataset/properties/football-key-stats/properties/name",
                            "type": "string"
                        },
                        "data": {
                            "$id": "#/properties/dataset/properties/football-key-stats/properties/data",
                            "type": "object",
                            "required": ["insight"],
                            "properties": {
                                "insight": {
                                    "$id": "#/properties/dataset/properties/football-key-stats/properties/data/properties/insight",
                                    "type": "array",
                                    "additionalItems": true,
                                    "items": {
                                        "$id": "#/properties/dataset/properties/football-key-stats/properties/data/properties/insight/items",
                                        "type": "object",
                                        "required": ["title", "statistics"],
                                        "properties": {
                                            "title": {
                                                "$id": "#/properties/dataset/properties/football-key-stats/properties/data/properties/insight/items/properties/title",
                                                "type": "string"
                                            },
                                            "statistics": {
                                                "$id": "#/properties/dataset/properties/football-key-stats/properties/data/properties/insight/items/properties/statistics",
                                                "type": "array",
                                                "additionalItems": true,
                                                "items": {
                                                    "$id": "#/properties/dataset/properties/football-key-stats/properties/data/properties/insight/items/properties/statistics/items",
                                                    "type": "string"
                                                }
                                            }
                                        }                                        
                                    }
                                }
                            }                            
                        }
                    }                    
                }
            }
        }
    }
}
```
{% endtab %}
{% endtabs %}

