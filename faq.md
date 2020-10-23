# FAQ

## How do I retrieve football probabilities for a match I have the Football API Id for?

If you have previously integrated with the Football API, getting back the relevant dataset for that match is simple.

Using the  [List Collection](api/reference/datasets/list-collection.md) endpoint you can request the dataset by passing in the match id, if you also pass in the full request parameter as true, it will return you back the full dataset saving you the need to make another request for the dataset detail.

```erlang
curl https://dataset.api.pamedia.io/v1/dataset?meta.matchId=14261&full=true
```

{% hint style="warning" %}
Please note that the above request will still return back a paginated payload so you must extract the first item from the array to retrieve the dataset.
{% endhint %}

