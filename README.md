# Quick-Notes-ElasticSearch

Notes about ElasticSearch

##

```
GET _cat/health?v

GET _cat/nodes?v

GET _cat/indices?v
```

```
# create index sales
PUT /sales

# create a document of type 'order' in index 'sales'
PUT /sales/order/123
{
  "orderID":"123",
  "amount":"200"
}

# get the document previously created
GET /sales/order/123

# delete 'sales' index 
DELETE /sales
```

## Load data

```shell
curl -s -H "Content-Type: application/x-ndjson" -X POST localhost:9200/_bulk --data-binary "@filename"

POST _bulk
```
x-ndjson => newline delimited json
