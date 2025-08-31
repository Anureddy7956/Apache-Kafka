## [Download apache kafka] (https://kafka.apache.org/downloads)

### First step to start zookepper server - open the downloaded kafka folder in terminal
use this following command
<pre>
cmd
  bin/zookeeper-server-start.sh config/zookeeper.properties
</pre>
#### Default port - 2181



<img width="1915" height="933" alt="Screenshot From 2025-08-31 23-28-40" src="https://github.com/user-attachments/assets/be506b66-6b82-4d3f-a386-c074a722f6e5" />


### Second step to start kafka/broker server - open the downloaded kafka folder in new terminal
use this following command
<pre>
  cmd
    bin/kafka-server-start.sh config/server.properties
</pre>
#### Default port - 9092

<img width="1915" height="548" alt="Screenshot From 2025-08-31 23-41-39" src="https://github.com/user-attachments/assets/777c8f66-870e-4fd3-a112-458a95d83386" />
