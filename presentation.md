---
title: "Presentation Elasticsearch and Kibana"
subtitle: ""
author: [Lana & Elena ]
#bibliography: paper.bib
date: "2021-11-06"
subject: ""
keywords: [Fontys, ESDE, workshop, elasticsearch, kibana#]
lang: "en"
titlepage: "true"
logo: "images/fontyslogo.png"
titlepage-rule-color: "400070"
#page-background : "images/fontyslogo-background.png"
# reveal settings
# simple black white league beige sky night serif simple solarized blood moon
theme: simple
separator: <!-- s -->
verticalSeparator: <!-- v -->
notesSeparator: <!-- n -->
revealOptions:
  # None - Fade - Slide - Convex - Concave - Zoom
  transition: 'slide'
  transition-speed: fast
  slideNumber: true
  history: true
  progress: true
  width: 1248
  height: 800
  #parallaxBackgroundImage: 'images/fontys-parallax-all-dark.jpg'
  parallaxBackgroundSize: '2100px 1024px'
  #autoSlide: 4000
  #loop: true

  # center: false
...
---

# Elasticsearch
![elasticserch](/images/elasticsearch-logo.svg)

<!-- s -->

## Content

- What is Elasticsearch? 
- What is Kibana? 
- What is the Elastic stack? 
- History of the Elastic Stack 
- Why Elasticsearch? 
- Key concepts of Elasticsearch 
- Use cases of Elasticsearch 
- Companies using Elasticsearch 
- Queries 
- Differences between Relational Database and Elasticsearch 
- How to get started with Elasticsearch? 
<!-- s -->

## What is Elasticsearch?
![elasticserch](/images/elasticsearch-logo.svg)

- Real-time distributed and open source full-text search and analytics engine
- developed in Java
- Based on the Lucene search engine
- Interaction through RESTful API
- uses schema less JSON documents to store data

<!-- s -->

## What is Kibana?
![kibana](/images/kibana-logo.svg)

- open source browser visualisation tool
- to visualize large amounts of data

<!-- s -->

## What is the Elastic stack?
![elasticstack](/images/elastic-stack-logo.svg)

- combination of the open source projects Elasticsearch, Logstash, Kibana and Beats

<!-- s -->
## History of the Elastic Stack
1. Elasticsearch developed as RESTful open source serach engine
2. Due to Elasticsearch being used more and more for log data, ingesting data and visualizing it became important so Logstash and Kibana were developed.
3. Beats added due to user suggestion



<!-- s -->

## Why Elasticsearch?
- compatible to run on every platform due to the development in java
- real time: newly added documents are directly searchable
- Handles multi-tenancy easily
- Scalability
- Performance
- Multilingual
- Document oriented -> json is easy to integrate
- autocompletion & instant search



<!-- s -->
## Key concepts of Elasticsearch

![ELK](/images/JsonVsData.png)


<!-- s -->

## Key concepts of Elasticsearch

- Document
- Index
- Shards
- Cluster
- Replica shards
- Node
- Type
- Mapping


<!-- s -->
## Index and shards
![ELK](/images/IndexAndShards.png)
<!-- s -->

## Use cases of Elasticsearch
- Full-text search
- Logging and Log Analysis
- Data visualization
- Scarping and combining public data
- Event data and metrics

<!-- s -->
## Elasticsearch Users
![ELK](/images/elasticsearch-users.jpeg)

<!-- s -->
## Companies using Elasticsearch
- Airbus (Elasticsearch For Real-Time Access to Aircraft Technical Documents)
- Netflix (integrated into their messaging platform that delivers messages to customers)
- slack (Monitor for malicious activity)

  
<!-- s -->
## Alternatives to Elasticsearch
- Apache Solr (open source based on Lucene)
  - queries can return in JSON, XML and CSV
  - Scalable only with help of SolrCloud
  - focused on text-based searching

<!-- s -->

## Queries
- Elasticsearch Query DSL
- Match All Query : "query": {  
      "match_all": { }  
- Full-text queries:  Match, multi_match


<!-- s -->

## Differences between Relational Database and Elasticsearch
![ELK](/images/db-vs-els.jpg)


<!-- s -->
 ## Solution Using Relational Database Query 
select * from product where name like '%Red%' or name like '%Shirt%'; 
![ELK](/images/databaseResult.png)
- Elasticsearch Solution
```
POST test/product/_search 
{      "query": { 
          "match": { 
            "name": "Red Shirt"   } } }
```

<!-- s -->
## Conclusion
![ELK](/images/elastickSolutoin.png)
- The differences will be in the result where Relational Database will return results in some random order while Elasticsearch returns results in decreasing order of _score which is calculated on the basis of relevancy. 

<!-- s -->

## How to get started with Elasticsearch?
- Is the Elasticsearch Alive?
- you can access it at  http://localhost:9200 on your web browser, which returns this:
![ELK](/images/ela-result.png)

<!-- s -->
## Elasticsearch
- Elasticsearch hides the complexities behind a REST API
POST (create)
GET (read)
PUT (update)
DELETE (delete)
- and curl can work fine as the following example: 
- ```curl -X PUT http://localhost:9200/newindex```
 
<!-- s -->

## Thank you for your attention
