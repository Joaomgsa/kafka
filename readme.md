# Queries the file readme.md from the repository


## Create a stream from a topic ksqlDB

```sql
CREATE STREAM pageviews_stream
  WITH (KAFKA_TOPIC='pageviews', VALUE_FORMAT='AVRO');

## To confirm that data is moving through your stream, you can run the following query: 

```sql
SELECT * FROM pageviews_stream EMIT CHANGES;


