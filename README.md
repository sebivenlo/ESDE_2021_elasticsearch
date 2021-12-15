# ESDE_2021_elasticsearch
Repository for the elasticsearch workshop


Generalized

Create an index:
```PUT Name-of-the-Index```


```
PUT Name-of-the-Index/_doc/id-you-want-to-assign-to-this-document
{
  "field": "value"
}
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
