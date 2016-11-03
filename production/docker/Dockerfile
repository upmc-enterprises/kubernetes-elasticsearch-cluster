FROM quay.io/pires/docker-elasticsearch-kubernetes:2.4.1
MAINTAINER Steve Sloka <slokas@upmc.edu>

# Builds: upmcenterprises/docker-elasticsearch-kubernetes:2.4.1

# Install kopf (https://github.com/lmenezes/elasticsearch-kopf)
RUN ./elasticsearch/bin/plugin install lmenezes/elasticsearch-kopf

# Install search-guard-ssl
RUN ./elasticsearch/bin/plugin install com.floragunn/search-guard-ssl/2.4.1.16

# Copy in SSL Certs
ADD node-keystore.jks /elasticsearch/config/node-keystore.jks
ADD truststore.jks /elasticsearch/config/truststore.jks

# Override elasticsearch.yml config
ADD elasticsearch.yml /elasticsearch/config/elasticsearch.yml
