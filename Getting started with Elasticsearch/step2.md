## Step 2 - Store Documents
Now cluster is up and running, we can insert documents using REST API.

    `curl -X PUT "localhost:9200/user/_doc/1?pretty" -H 'Content-Type: application/json' -d'
    {
    "name": "Amit Jha"
    }
    '
    ` {{execute}}



    `curl -X PUT "localhost:9200/user/_doc/2?pretty" -H 'Content-Type: application/json' -d'
    {
    "name": "Kabir Jha"
    }
    '
    ` {{execute}}



    `curl -X PUT "localhost:9200/user/_doc/3?pretty" -H 'Content-Type: application/json' -d'
    {
    "name": "John Smith"
    }
    '
    ` {{execute}}