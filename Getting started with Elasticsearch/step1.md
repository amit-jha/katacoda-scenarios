## Setup Elasticsearch container using docker. 
To get started, we shall be launching elasticsearch single node cluster.

`docker run --name es -p 9200:9200 -e "discovery.type=single-node" elasticsearch:7.11.2`{{execute}}


### Test Elasticsearch Setup 

`curl localhost:9200`{{execute}}