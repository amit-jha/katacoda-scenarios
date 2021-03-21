## Search documents

Retrieve all documents 

`curl -X GET "localhost:9200/user/_search?pretty" -H 'Content-Type: application/json' -d'
{
"query": { "match_all": {} }
}
'
`{{execute}}

Search documents by fiels

`curl -X GET "localhost:9200/user/_search?pretty" -H 'Content-Type: application/json' -d'
{
"query": { "match": {
    "name": "Amit Jha"
} }
}
'
`{{execute}}
