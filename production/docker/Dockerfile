FROM quay.io/pires/docker-elasticsearch-kubernetes:2.4.1
MAINTAINER Steve Sloka <slokas@upmc.edu>

# Builds: upmcenterprises/docker-elasticsearch-kubernetes:2.4.1

# Install kopf (https://github.com/lmenezes/elasticsearch-kopf)
RUN ./elasticsearch/bin/plugin install lmenezes/elasticsearch-kopf

# Install search-guard-ssl
RUN ./elasticsearch/bin/plugin install com.floragunn/search-guard-ssl/2.4.1.16

# Override elasticsearch.yml config
ADD elasticsearch.yml /elasticsearch/config/elasticsearch.yml
