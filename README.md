# INTEGRATION_Jenkins

Visualizations and dashboard for showing Jenkins devOps performances

## Installing

- Query for all documents of kibana index

*curl -XGET 'http://localhost:9223/.kibana/_search?pretty' -H 'Content-Type: application/json' -d'
{
	"size": 10000,
	"query": {
        "match_all": {}
    }
}
' > kibana.txt*

- Get current Jenkins index pattern id. For example:

*"_index" : ".kibana",
        "_type" : "doc",
        "_id" : "index-pattern:23c9b990-8f18-11e8-9f63-5f797506860e",
        "_score" : 1.0,
        "_source" : {
          "type" : "index-pattern",
          "updated_at" : "2018-07-24T08:04:09.140Z",
          "index-pattern" : {
            "title" : "jenkins",*


- Change index pattern ID on each visualization accordingly 
- Import visualizations and dashboard in Kibana

## Authors

* **andrea.cesaro@keypartner.it** - *Initial work*
