---
# Solutions to the Assignments

## Task 1

1.1 Create an index for the accounts of employees of a company.
```PUT employees```

1.2 Add a person with a first name, a last name and a job title.
```
PUT employees/_doc/0
{
  "first_name": "Emma",
  "last_name" : "Watson",
  "job_title" : "actor"
}
```

1.3 Retrieve the created account
```GET employees/_doc/0```

1.4 Update the document by adding the field ‘birth_date’.
```
POST employees/_update/0
{
  "doc": {
    "birth_date": "16.01.1996"
  }
} 
```

1.5 Add a second person with the same job title.
```
PUT employees/_doc/1
{
  "first_name":"Daniel",
  "last_name" : "Radcliff",
  "job_title" : "actor"
}
```

1.6 Search for the persons based on their jobtitle.
```
GET employees/_search
{
  "query": {
    "match": {
      "job_title": "actor"
    }
  }  
}
```
1.7 Delete an account.
```DELETE employees/_doc/1 ```


## Task 2

2.1 Get all the documents in the dataset with the match_all query.
```
GET /shakespeare/_search
{
    "query": {
            "match_all": {}
    }
}
```

2.2 Search for the lines in which the ‘play_name’ is ‘Timon of Athens’ with the match query.
```
GET /shakespeare/_search
{
  "query" :{
    "match":{
      "play_name": " Timon of Athens"
    }
  }
}
```

2.3 Search for the lines in the play ‘Hamlet’ (‘play_name’) in which the ‘speaker’ is ‘BERNARDO’.
```
GET /shakespeare2/_search
{
  "query" :{
    "bool": {
      "must": [
        {
          "match": {
            "play_name": "Hamlet"
          }
        },
        {
          "match": {
            "speaker": "BERNARDO"
          }
        }
      ]
    }
  }
}
```

2.4 Search for the lines with the word ‘christmas’.
```
GET shakespeare/_search
{
  "query": {
    "match": {
      "text_entry": {
        "query": "christmas"
      }
    }
  }
}

```


