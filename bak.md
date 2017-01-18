PHP Fatal error:  Uncaught exception 'Elasticsearch\Common\Exceptions\BadRequest400Exception' 
with message '{"error":{"root_cause":[{"type":"parse_exception","reason":"Failed to derive xcontent"}]
,"type":"parse_exception","reason":"Failed to derive xcontent"},"status":400}' in 
/libs/vendor/elasticsearch/elasticsearch/src/Elasticsearch/Connections/Connection.php:681
Stack trace:
#0 /libs/vendor/elasticsearch/elasticsearch/src/Elasticsearch/Connections/Connection.php(659): 
Elasticsearch\Connections\Connection->tryDeserializeError(Array, 'Elasticsearch\\C...')

#1 /libs/vendor/elasticsearch/elasticsearch/src/Elasticsearch/Connections/Connection.php(579): 
Elasticsearch\Connections\Connection->tryDeserialize400Error(Array)

#2 /libs/vendor/elasticsearch/elasticsearch/src/Elasticsearch/Connections/Connection.php(261): 
Elasticsearch\Connections\Connection->process4xxError(Array, Array, Array)

#3 /var/www/vhost in /libs/vendor/elasticsearch/elasticsearch/src/Elasticsearch/Connections/Connection.php on line 682
