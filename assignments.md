---
title: Elasticsearch workshop assignments
---

Assignments
=====

To do the assignments run the docker commands to create two docker containers - one for Elasticsearch and one for Kibana.
Access the Kibana dashboard at [http://localhost:5601](http://localhost:5601) and navigate to the dev tool.

## Task 1: Simple Query Assignment

In this assignment you are to create a system for the employees of a company. Every employee is to have an account in this system containing the first name, last name and job title.

1. Create an index for the accounts of employees of a company.
2. Add a person to the accounts  /add an account for a person with a first name, a last name and a job title.
3. Retrieve the created account
4. Update the document by adding the field 'birth_date'.
5. Add a second person with the same job title.
6. Search for the persons based on their jobtitle. (e.g if you added teachers to elasticsearch then search for the employees with the job title 'teacher')
7. Delete an account.


## Task 2:  More advanced search with a bigger dataset

In this assignment we want to play a bit with a bigger dataset - the Shakespeare dataset. A dataset containing lines out of Shakespeare plays 
Steps to take before starting:
- Download the shakespeare.json file from the repository.
- Add the data to Elasticsearch over Kibana by following these steps:
  - Choose to upload your own data in the home screen.
  - Change the number_of_lines parameter to 40000 (This does not add the full file but adds a big enough dataset containing multiple plays).
  - Click import
  - Choose the advanced method to view the mapping that is created and set the index to 'shakespeare'.

The mapping of the shakespeare dataset should look as follows.

´´´
{
  "properties": {
    "index": {
      "type": "object"
    },
    "line_id": {
      "type": "long"
    },
    "line_number": {
      "type": "keyword"
    },
    "play_name": {
      "type": "keyword"
    },
    "speaker": {
      "type": "keyword"
    },
    "speech_number": {
      "type": "keyword"
    },
    "text_entry": {
      "type": "text"
    }
  }
}
´´´

Now to the queries:
1. Get all the documents in the dataset with the match_all query.
2. Search for the scenes in which the 'play_name' is 'Timon of Athens' with the match query.
3. Search for the scenes in the play 'Hamlet' ('play_name') in which the 'speaker' is 'Bernardo'. Tip: boolean conditions & match query


### Some useful links for the assignments

- https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-index_.html
- https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-update.html
- https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-get.html
- https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-delete.html
- https://www.elastic.co/guide/en/elasticsearch/reference/current/search-your-data.html
- https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-match-all-query.html
- https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-match-query.html
- https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-bool-query.html
- https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html
