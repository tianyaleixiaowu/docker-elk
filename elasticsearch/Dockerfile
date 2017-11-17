# https://github.com/elastic/elasticsearch-docker
#注意，我没有使用docker-compose，而是采用分别打3个docker来部署的，所以需要把compose里的配置抄到这里来
FROM docker.elastic.co/elasticsearch/elasticsearch:5.6.3
COPY config/elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml
# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
