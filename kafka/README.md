```sh
docker pull apache/kafka:3.9.1
docker run -name kafka -p 9092:9092 apache/kafka:3.9.1
docker exec -it kafka sh
```
In de container:
```sh
cd /opt/kafka
bin/kafka-topics.sh --create --topic quickstart-events --bootstrap-server localhost:9092  # Create topic
bin/kafka-topics.sh --describe --topic quickstart-events --bootstrap-server localhost:9092 # Describe topic
bin/kafka-topics.sh --list --bootstrap-server localhost:9092 # List all topics
bin/kafka-console-producer.sh --topic quickstart-events --bootstrap-server localhost:9092 # Add events
bin/kafka-console-consumer.sh --topic quickstart-events --from-beginning --bootstrap-server localhost:9092 # Read events
```