# https://github.com/elastic/elasticsearch-docker
#注意，我没有使用docker-compose，而是采用分别打3个docker来部署的，所以需要把compose里的配置抄到这里来
#注意一个地方，当持久化ES的data时。看下面的说明，要求主机的/path/to/storage目录必须被主机的uid为1000的用户所拥有，这是写死的。uid1000需要对该目录具备完全权限
#注意环境变量ELASTIC_PASSWORD: changeme，用的是fork的那个xpack分支

#How can I persist Elasticsearch data?
#The data stored in Elasticsearch will be persisted after container reboot but not after container removal.
#In order to persist Elasticsearch data even after removing the Elasticsearch container, you'll have to mount a volume on your Docker host. Update the elasticsearch service declaration to:
#elasticsearch:

#  volumes:
#    - /path/to/storage:/usr/share/elasticsearch/data
# This will store Elasticsearch data inside /path/to/storage.

# NOTE: beware of these OS-specific considerations:

# Linux: the unprivileged elasticsearch user is used within the Elasticsearch image, therefore the mounted data directory must be owned by the uid 1000.
# macOS: the default Docker for Mac configuration allows mounting files from /Users/, /Volumes/, /private/, and /tmp exclusively. Follow the instructions from the documentation to add more locations.
#FROM docker.elastic.co/elasticsearch/elasticsearch:5.6.3
FROM docker.elastic.co/elasticsearch/elasticsearch-basic:6.1.0
COPY config/elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml
VOLUME /usr/share/elasticsearch/data
# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
