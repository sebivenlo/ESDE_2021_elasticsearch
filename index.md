## Elasticsearch workshop

This is a workshop about elasticsearch created for the module ESDE.


### How to prepare for the workshop

In the workshop you will be solving assignments in a Docker container.
To create the Docker container with elasticsearch and kibana run the following commands:

```
docker network create elastic
docker pull docker.elastic.co/elasticsearch/elasticsearch:7.15.2
docker run --name es01-test --net elastic -p 127.0.0.1:9200:9200 -p 127.0.0.1:9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.15.2

docker pull docker.elastic.co/kibana/kibana:7.15.2
docker run --name kib01-test --net elastic -p 127.0.0.1:5601:5601 -e "ELASTICSEARCH_HOSTS=http://es01-test:9200" docker.elastic.co/kibana/kibana:7.15.2
```

Then you can access the kibana container under (http://localhost:5601)

### Slides for the workshop

The information of the slides can be found on [this](https://sebivenlo.github.io/ESDE_2021_elasticsearch/presentation.html) page.




### Markdown for this file

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

