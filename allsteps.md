# Getting started with Elasticsearch

## Step 1 - Run Elasticsearch
`docker run --name es -p 9200:9200 -e "discovery.type=single-node" elasticsearch:7.11.2` {{execute}}

* Test Setup

    `curl localhost:9200` {{execute}}

## Step 2 - Store some documents
* Insert some documents 

* Document 1 

`curl -X PUT "localhost:9200/user/_doc/1?pretty" -H 'Content-Type: application/json' -d'
{
  "name": "Amit Jha"
}
'
` {{execute}}

* Document 2 

`curl -X PUT "localhost:9200/user/_doc/2?pretty" -H 'Content-Type: application/json' -d'
{
  "name": "Kabir Jha"
}
'
` {{execute}}

* Document 3 

`curl -X PUT "localhost:9200/user/_doc/3?pretty" -H 'Content-Type: application/json' -d'
{
  "name": "John Smith"
}
'
` {{execute}}



## Step 3 - Search documents

* Retrieve all documents 

`curl -X GET "localhost:9200/user/_search?pretty" -H 'Content-Type: application/json' -d'
{
  "query": { "match_all": {} }
}
'
` {{execute}}

* Search documents by fiels

`curl -X GET "localhost:9200/user/_search?pretty" -H 'Content-Type: application/json' -d'
{
  "query": { "match": {
      "name": "Amit Jha"
  } }
}
'
` {{execute}}


