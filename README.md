nc localhost 5000 < /home/marina/logs/*.log



curl -XPOST -D- 'http://localhost:5601/api/saved_objects/index-pattern' \
    -H 'Content-Type: application/json' \
    -H 'kbn-version: 6.3.0' \
    -d '{"attributes":{"title":"logstash-*","timeFieldName":"@timestamp"}}'
