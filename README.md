## Prerequisities
JDK8
Zookeeper
Kafka
Maven

## Getting Started
- Install the respected Zookeeper and kafka binary files 
#### Install Jdk8
Open command prompt as administrator
- choco install jdk8

#### Install Maven
Open command prompt as administrator
- choco install maven

#### Configuration
Configure both zookeeper and kafka

##### Zookeeper
Create the required zoo.cfg. In C:\apache-zookeeper-3.5.6-bin\conf, copy zoo_sample.cfg to zoo.cfg. Open zoo.cfg in Notepad++. Find and edit dataDir=/tmp/zookeeper to dataDir=C:\apache-zookeeper-3.5.6-bin\data

##### Kafka
For convenience, copy the C:\kafka_2.12-2.2.0\config\server.properties file from the config folder to the C:\kafka_2.12-2.2.0\bin\windows folder. Open server.properties in Notepad++. Find and edit log.dirs=/tmp/kafka-logs to log.dirs=C:\kafka_2.12-2.2.0\logs

#### Start Zookeeper
zkserver

#### Start Kafka
Open Command prompt in C:\kafka_2.12-2.3.0\bin\windows folder
.\kafka-server-start.bat .\server.properties

#### Compile and Build Jar File
Open Command Prompt as Admin in root folder
mvn clean compile assembly:single

#### Start Producer
java -cp target/kafka-api-1.0-SNAPSHOT-jar-with-dependencies.jar com.spnotes.kafka.simple.Producer test

#### Start Consumer
java -cp target/kafka-api-1.0-SNAPSHOT-jar-with-dependencies.jar com.spnotes.kafka.simple.Consumer test group1

#### Running

This kakfa application allows us to display the messages typed in producer in our consumer command prompt.







