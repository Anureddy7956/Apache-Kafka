# To Creating a topic
while creating a topic name(wave0) we should enter kafka server name(bootstrap), local host along with the port (9092) and also define number of partitions in each broker and replication factor 
<pre>
  bash

    bin/kafka-topics.sh --bootstrap-server localhost:9092 --create --topic wave0-topic --partitions 3 --replication-factor 1
</pre>

# To read or describe 
describe shows how many partitions are created in a topic 
<pre>
  bash

    bin/kafka-topics.sh --bootstrap-server localhost:9092 --describe --topic wave0-topic
</pre>

# Update or alter
<pre>
  bash

     bin/kafka-topics.sh --bootstrap-server localhost:9092 --alter --topic wave-topic --partitions 4

</pre>

# Delete a topic
<pre>
  bash

     bin/kafka-topics.sh --bootstrap-server localhost:9092 --delete --topic wave0-topic

</pre>
