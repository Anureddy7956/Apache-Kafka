# Step 1:Start zookeeper server
<pre>
  bash
  
     bin/zookeeper-server-start.sh config/zookeeper.properties  
</pre>
<img width="1920" height="331" alt="Screenshot From 2025-09-03 08-31-43" src="https://github.com/user-attachments/assets/e79844da-d19f-4147-a4cd-07694d9d697b" />


# Step 2:Start kafka server 
<pre>
  bash
    bin/kafka-server-start.sh config/server.properties
</pre>
<img width="1920" height="331" alt="Screenshot From 2025-09-03 08-37-21" src="https://github.com/user-attachments/assets/bac2cd8b-e1c5-4b74-a7a7-ea40f9420fe5" />


# Step 3: Create a chat topic

<pre>
  bash 
    
     bin/kafka-topics.sh --create --topic chat-topic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1
</pre>
  <img width="1920" height="109" alt="Screenshot From 2025-09-03 08-43-24" src="https://github.com/user-attachments/assets/a24586e8-786f-4a64-a2ce-d8be9edaa593" />


## Describe a chat topic
<pre>
  bash 
    
    bin/kafka-topics.sh --describe --topic chat-topic --bootstrap-server localhost:9092
</pre>

<img width="1920" height="138" alt="Screenshot From 2025-09-03 08-46-49" src="https://github.com/user-attachments/assets/2b3a1054-caf0-47bb-bbb4-3b29e4b273c2" />


## Alter the topic 
replication factor is not used 
<pre>
  bash
    
    bin/kafka-topics.sh --alter --topic chat-topic --bootstrap-server localhost:9092 --partitions 3 
</pre>
<img width="1920" height="362" alt="Screenshot From 2025-09-03 08-49-51" src="https://github.com/user-attachments/assets/2ee7192f-d3e2-470e-9f40-3609e3a8c7f0" />

 
# Step 3:Open consumer(reciever)

 <pre>
   bash
     
     bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic chat-topic --from-beginning
 </pre>

 <img width="1920" height="151" alt="Screenshot From 2025-09-03 08-56-46" src="https://github.com/user-attachments/assets/983e8117-f4d5-4d5c-8568-e1aff9bc107f" />



# Step 4:Open producer(sender)

<pre>
  bash
   
     bin/kafka-console-producer.sh --bootstrap-server localhost:9092 --topic chat-topic 
</pre>
 
<img width="1920" height="151" alt="Screenshot From 2025-09-03 09-01-51" src="https://github.com/user-attachments/assets/e273bf8b-fd31-43f2-aa1b-0cc5323bd1a0" />

