## Test Elasticsearch Setup. 
To get started, we need to ensure that elasticsearch is up and running. To test run `curl localhost:9200`{{execute}} 

You should see output identical to following 

`
{
  "name" : "WsrZMDZ",
  "cluster_name" : "docker-cluster",
  "cluster_uuid" : "eMnDljciRGqumzL7-7SCBw",
  "version" : {
    "number" : "6.2.2",
    "build_hash" : "10b1edd",
    "build_date" : "2018-02-16T19:01:30.685723Z",
    "build_snapshot" : false,
    "lucene_version" : "7.2.1",
    "minimum_wire_compatibility_version" : "5.6.0",
    "minimum_index_compatibility_version" : "5.0.0"
  },
  "tagline" : "You Know, for Search"
}
`