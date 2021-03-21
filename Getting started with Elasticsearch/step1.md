## Elasticsearch Setup. 
To get startet, First elasticsearch should be installed. In this scenario, we'll be setting up Elaticsearch container. Lets start the test drive.

### Setup Task
`docker run -d --name es -p 9200:9200 -e "discovery.type=single-node" elasticsearch:7.11.2`{{execute}}

Once Elasticsearch is setup, Lets validate the setup.

### Validate Task
`curl localhost:9200`{{execute}} 

You should see output somewhat identical to following 

`{
  "name" : "1f9ad98260bd",
  "cluster_name" : "docker-cluster",
  "cluster_uuid" : "y9T_pTjdRyu8MVjoQFgTjQ",
  "version" : {
    "number" : "7.11.2",
    "build_flavor" : "default",
    "build_type" : "docker",
    "build_hash" : "3e5a16cfec50876d20ea77b075070932c6464c7d",
    "build_date" : "2021-03-06T05:54:38.141101Z",
    "build_snapshot" : false,
    "lucene_version" : "8.7.0",
    "minimum_wire_compatibility_version" : "6.8.0",
    "minimum_index_compatibility_version" : "6.0.0-beta1"
  },
  "tagline" : "You Know, for Search"
}`