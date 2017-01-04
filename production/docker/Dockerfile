FROM quay.io/pires/docker-elasticsearch-kubernetes:5.1.1
MAINTAINER Steve Sloka <slokas@upmc.edu>

# Builds: upmcenterprises/docker-elasticsearch-kubernetes:5.1.1

# Install mapper-attachments (https://www.elastic.co/guide/en/elasticsearch/plugins/5.x/mapper-attachments.html)
RUN ./elasticsearch/bin/elasticsearch-plugin install mapper-attachments

# Install search-guard-ssl
RUN ./elasticsearch/bin/elasticsearch-plugin install -b com.floragunn:search-guard-ssl:5.1.1-18

# Install s3 repository plugin
RUN ./elasticsearch/bin/elasticsearch-plugin install repository-s3

# Override elasticsearch.yml config
ADD elasticsearch.yml /elasticsearch/config/elasticsearch.yml
