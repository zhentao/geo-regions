# geo-regions
The file regions can be created using the following command:
```
curl https://restcountries.eu/rest/v1/all | jq -c '.[] | {"index": {"_index": "regions", "_id": .alpha3Code}}, {name: .name, location: [.latlng[1], .latlng[0]] }' > regions
```
