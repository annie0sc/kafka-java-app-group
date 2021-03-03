# kafka-java-app-group

## Group Members:

<table>
<td align="center"><a href="https://github.com/annie0sc"><img src="https://avatars.githubusercontent.com/u/28427324?s=460&u=31b810c008419d5bfb81c152d51ec90cb96dc28b&v=4" width="100px;" alt=""/><br /><sub><b>Annie Chandolu</b></sub></a><br /></td>
<td align="center"><a href="https://github.com/alekhyajaddu"><img src="https://avatars.githubusercontent.com/u/60018848?s=460&u=7cc6d01354b7857d88890a77b510232333fb9b53&v=4" width="100px;" alt=""/><br /><sub><b>Alekhya Jaddu</b></sub></a><br /></td>
<td align="center"><a href="https://github.com/SwaroopReddyGottigundala"><img src="https://avatars.githubusercontent.com/u/60024334?s=460&u=20ef224b43a8e817fdceb9e558d631e1a6e7435d&v=4" width="100px;" alt=""/><br /><sub><b>Swaroop Reddy</b></sub></a><br /></td>
<td align="center"><a href="https://github.com/KHARIKA17"><img src="https://avatars.githubusercontent.com/u/60010885?s=460&u=24c5428d5a37b37a3efd752d271740b402177734&v=4" width="100px;" alt=""/><br /><sub><b>Harika Kulkarni</b></sub></a><br /></td>
</table>

## Annie Chandolu - Team Lead

Hello! I have used the random funtion to generate a ssentence which displays a date and it's day. It may or may not be the exact day. 

[Link to my code](https://github.com/annie0sc/kafka-java-app-group/blob/main/src/main/java/nwmsu/bigdata/kafkajava/sec01/group02/ProducerByAnnie.java) 

#### Commands used:

I have used the following commands to run:

1. Start Zookeeper in your kafka folder on C drive.
```
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```
1. Start Kafka in the same folder as above.
```
.\bin\windows\kafka-server-start.bat .\config\server.properties
```
1. Creat a new topic and list all of them in the same folder. I have created a new topic called annies-part2-messages.
```
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic annies-part2-messages
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list
```
1. Then open your code folder and run the MVN command to compile the code.
```
mvn clean compile assembly:single
```
1. Once the build is complete, start the Consumer using your artifact ID, group ID and topic name.
```
java -cp target/kafka-java-app-group-1.0-SNAPSHOT-jar-with-dependencies.jar nwmsu.bigdata.kafkajava.sec01.group02.Consumer annies-part2-messages group02
```
1. Then start the Producer in the same folder.
```
java -cp target/kafka-java-app-group-1.0-SNAPSHOT-jar-with-dependencies.jar nwmsu.bigdata.kafkajava.sec01.group02.ProducerByAnnie annies-part2-messages
```
Voila! Your app will run!

#### References:

1. [Dr. Case's Twitter Example](https://github.com/denisecase/kafka-case)
1. [Dr. Case's Kafka Example](https://github.com/denisecase/kafka-api)
1. [Gundu Pooja's Group](https://github.com/GUNDUPOOJA/kafka-java-app)

## Team Members
## Alekhya Jaddu
For my custom producer package I have used the days of week and type of weather. The messages which will be displayed are days of the week and the type of weather on that day, joined by a verb.
### Setting up the Kafka environment
* Open PowerShell in C:\kafka_2.13-2.7.0 folder.

* Use a different PowerShell window for each process.

Window 1 - Run Zookeeper Service (keep window open)
```
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```
Window 2 - Run Kafka Service (keep window open)
```
.\bin\windows\kafka-server-start.bat .\config\server.properties
```
Window 3  - Create your topic name
```
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic alex-kafka
```
### Compile and build the jar file
Open PowerShell as Administrator in your root project folder
```
mvn clean compile assembly:single
```
### Start Producer
```
java -cp target/kafka-java-app-group-1.0-SNAPSHOT-jar-with-dependencies.jar nwmsu.bigdata.kafkajava.sec01.group02.ProducerByAlex alex-kafka
```
### Start Consumer
```
java -cp target/kafka-java-app-group-1.0-SNAPSHOT-jar-with-dependencies.jar nwmsu.bigdata.kafkajava.sec01.group02.Consumer alex-kafka group02
```
## Swaroop Reddy Gottigundala
 I have randomly generated the lyrics of the song "My Life is going on" by Cecilia Krull for my custom producer package.
### Kafka commands
Window 1 - Run Zookeeper service
```
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```
Window 2 - Run Kafka Service 
```
.\bin\windows\kafka-server-start.bat .\config\server.properties
```
Window 3  - Create your topic name
```
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic sunny-messages
```
Window 4 - Compile the jar file
```
mvn clean compile assembly:single
```
Window 5 - Start Producer
```
java -cp target/kafka-java-app-group-1.0-SNAPSHOT-jar-with-dependencies.jar nwmsu.bigdata.kafkajava.sec01.group02.ProducerBySunny sunny-messages
```
Window 6 - Start Consumer
```
java -cp target/kafka-java-app-group-1.0-SNAPSHOT-jar-with-dependencies.jar nwmsu.bigdata.kafkajava.sec01.group02.Consumer sunny-messages group02
```
## Harika Kulkarni
I have generated a random sentencen using Articles,noun,verb,preposition.
### Steps involved:
Step1: In Kafka Folder,open powershell as Admin and start Zookeeper service as below:
```
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```
Step2: In Kafka Folder,open another powershell as Admin and start Kafka service as below:
```
.\bin\windows\kafka-server-start.bat .\config\server.properties
```
Step3: In Kafka Folder,open another powershell as Admin and create a topic
```
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic random-text
```
Step4: In root project folder,open Powershell as admin and compile the code using the below command.
```
mvn clean compile assembly:single
```
Step5: In the same root project folder,start the Consumer using another terminal
```
java -cp target/kafka-java-app-group-1.0-SNAPSHOT-jar-with-dependencies.jar nwmsu.bigdata.kafkajava.sec01.group02.Consumer random-text group02
```
Step6: In the same root project folder,start the Producer using another terminal
```
java -cp target/kafka-java-app-group-1.0-SNAPSHOT-jar-with-dependencies.jar nwmsu.bigdata.kafkajava.sec01.group02.ProducerByHarika random-text
```

