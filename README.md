# ESDE_2021_elasticsearch
Repository for the elasticsearch workshop


Generalized

Create an index:
```PUT Name-of-the-Index```

Create a document
```
PUT Name-of-the-Index/_doc/id-you-want-to-assign-to-this-document
{
  "field": "value"
}
```
Read a document
```
GET Name-of-the-Index/_doc/id-of-the-document-you-want-to-retrieve
```


Update a document
```
POST Name-of-the-Index/_update/id-of-the-document-you-want-to-update
{
  "doc": {
    "field1": "value",
    "field2": "value",
  }
} 
```


Delete an index
```
DELETE Name-of-the-Index/_doc/id-of-the-document-you-want-to-delete
```

