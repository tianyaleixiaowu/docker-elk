# https://github.com/elastic/logstash-docker
FROM docker.elastic.co/logstash/logstash:5.6.3
#FROM docker.elastic.co/logstash/logstash-x-pack:6.1.0
COPY config/logstash.yml /usr/share/logstash/config/logstash.yml
ADD pipeline/logstash.conf /usr/share/logstash/pipeline/
# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
