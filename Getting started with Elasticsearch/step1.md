## Elasticsearch Setup. 
To get startet, First elasticsearch should be installed. In scenario, we'll be setting up Elaticsearch container. Lets begin the test drive.

### Setup Task
`docker run --name es -p 9200:9200 -e "discovery.type=single-node" elasticsearch:7.11.2`{{execute}}

Once Elasticsearch is setup, Lets validate the setup.
### Validate Task
`curl localhost:9200`{{execute}} 

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