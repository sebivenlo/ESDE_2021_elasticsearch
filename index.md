# Elasticsearch workshop

This is a workshop about Elasticsearch created for the module ESDE.


## How to prepare for the workshop

In the workshop you will be solving assignments in a Docker container.
To create a Docker container with Elasticsearch and a Docker container with Kibana run the following commands:

```
docker network create elastic
docker pull docker.elastic.co/elasticsearch/elasticsearch:7.15.2
docker run --name es01-test --net elastic -p 127.0.0.1:9200:9200 -p 127.0.0.1:9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.15.2

docker pull docker.elastic.co/kibana/kibana:7.15.2
docker run --name kib01-test --net elastic -p 127.0.0.1:5601:5601 -e "ELASTICSEARCH_HOSTS=http://es01-test:9200" docker.elastic.co/kibana/kibana:7.15.2
```

Then you can access the Kibana container under [http://localhost:5601](http://localhost:5601)

## Slides for the workshop

The information of the slides can be found on [this](https://sebivenlo.github.io/ESDE_2021_elasticsearch/presentation.html) page but also as a pdf in the repository.


## Assignments for the workshop

The assignments of the workshop can be found [here](https://sebivenlo.github.io/ESDE_2021_elasticsearch/assignments.html).

## Small Cheat sheet

For the first assignments there is a small cheat sheet [here](https://sebivenlo.github.io/ESDE_2021_elasticsearch/cheat_sheet.html).


## Sources

- [official website](https://www.elastic.co/de/)
- [Elastic Documentation](https://www.elastic.co/guide/index.html)
- [https://stackshare.io/stackups/elasticsearch-vs-kibana](https://stackshare.io/stackups/elasticsearch-vs-kibana)
- [https://www.section.io/blog/elasticsearch-and-kibana/](https://www.section.io/blog/elasticsearch-and-kibana/)
- [https://medium.com/@victorsmelopoa/an-introduction-to-elasticsearch-with-kibana-78071db3704](https://medium.com/@victorsmelopoa/an-introduction-to-elasticsearch-with-kibana-78071db3704)
- [http://workshopdudes.github.io/elasticsearch-workshop-slides/#/](http://workshopdudes.github.io/elasticsearch-workshop-slides/#/)
- [https://opensourcelibs.com/lib/elasticsearch-workshop](https://opensourcelibs.com/lib/elasticsearch-workshop)
- [https://alternativeto.net/software/elasticsearch/](https://alternativeto.net/software/elasticsearch/) 


### Tutorials
- [https://dev.to/elastic/performing-crud-operations-with-elasticsearch-kibana-50ka](https://dev.to/elastic/performing-crud-operations-with-elasticsearch-kibana-50ka)
- [https://www.elastic.co/de/blog/a-practical-introduction-to-elasticsearch](https://www.elastic.co/de/blog/a-practical-introduction-to-elasticsearch)
- [https://www.tutorialspoint.com/elasticsearch/index.htm](https://www.tutorialspoint.com/elasticsearch/index.htm)


