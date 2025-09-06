## Step 1: Start zookeeper server
<pre>
  bash
  
     bin/zookeeper-server-start.sh config/zookeeper.properties  
</pre>
<img width="1920" height="331" alt="Screenshot From 2025-09-03 08-31-43" src="https://github.com/user-attachments/assets/e79844da-d19f-4147-a4cd-07694d9d697b" />


## Step 2: Start kafka server 
<pre>
  bash
    bin/kafka-server-start.sh config/server.properties
</pre>
<img width="1920" height="331" alt="Screenshot From 2025-09-03 08-37-21" src="https://github.com/user-attachments/assets/bac2cd8b-e1c5-4b74-a7a7-ea40f9420fe5" />


## Step 3: Create a chat topic

<pre>
  bash 
    
     bin/kafka-topics.sh --create --topic chat-topic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1
</pre>
  <img width="1920" height="109" alt="Screenshot From 2025-09-03 08-43-24" src="https://github.com/user-attachments/assets/a24586e8-786f-4a64-a2ce-d8be9edaa593" />
 
## Step 3: Open consumer(reciever)

 <pre>
   bash
     
     bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic chat-topic --from-beginning
 </pre>

 <img width="1920" height="151" alt="Screenshot From 2025-09-03 08-56-46" src="https://github.com/user-attachments/assets/983e8117-f4d5-4d5c-8568-e1aff9bc107f" />

## Step 4: Open producer(sender)

<pre>
  bash
   
     bin/kafka-console-producer.sh --bootstrap-server localhost:9092 --topic chat-topic 
</pre>
 
<img width="1920" height="151" alt="Screenshot From 2025-09-03 09-01-51" src="https://github.com/user-attachments/assets/e273bf8b-fd31-43f2-aa1b-0cc5323bd1a0" />

## Chat demo system in terminal


<img width="1920" height="880" alt="Screenshot From 2025-09-03 09-38-40" src="https://github.com/user-attachments/assets/e133e50b-2672-4694-9950-b6a03beb5fdd" />
  Left hand side - Producer    _______________________________________________________________                                                                                           Right hand side -Consumer 
                    

                    
Producer-> produces the message(sender)


Consumer-> consumes the message(reciever)


## In offset explorer(GUI)

<img width="1920" height="1011" alt="Screenshot From 2025-09-03 09-42-25" src="https://github.com/user-attachments/assets/090a0070-aa70-4fe8-9cab-60e6a85ec086" />


