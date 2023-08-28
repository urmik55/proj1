
# Intelligence Measurement System Project-Real-time Air Traffic Monitoring Platform

A brief description of what this project does and who it's for


## Author
Urmik Kanjaria (191887)
## Introduction
This project aims to design and implement a real-time analytical platform to monitor air traffic in Poland. The project uses data from the AviationStack API, which provides real-time flight information, including flight schedules, flight status, and flight tracking.

The platform is designed to be scalable and distributed, making use of Spark and queueing systems. The system architecture allows for real-time data processing and analysis, allowing the user to monitor air traffic patterns and detect anomalies.
## Technologies used
AWS EMR/Spark/Python/Scala/Java

## Data Source
The AviationStack API provides real-time flight data, including flight schedules, flight status, and flight tracking. The data is available in JSON format and is updated in real-time.
## Data Processing
I have tried following methods:

AWS Kinesis- Kinesis allows us to ingest and process high volumes of real-time data.

Kinesis Data Stream:  Kinesis allows us to ingest and process high volumes of real-time data.

Kinesis Producer: It would be responsible for receiving data from the AviationStack API and sending it to the Kinesis Data Stream.

Kinesis Consumer: It would be responsible for reading the processed data from the Kinesis Data Stream. It could also be responsible for triggering any alerts or notifications based on the analyzed data.

 I used a kinesis queue. My concept is to run kinesis producer which gets data from API and puts it to queue. Then a consumer will be running simultaneously. It will take data from queue and compute something.
 First it should run datastream. Then run simultaneously consumer and producer. Consumer will wait for a certain number of data (in while loop), so producer must be ran few times.


Well, we can implement this project just by using Apache Spark without the need for a messaging system like Kafka or Kinesis:
The data can then be analyzed to provide insights into air traffic patterns in Poland.
## Deployment
The system is deployed on AWS EMR, a fully managed cloud service that allows for the easy deployment and management of Spark clusters. 
## Visualizing the data on the map
The map shows the scattering path of flights passing over Poland.
It can also display other relevant information, such as flight number, altitude, speed, and destination.
## Problems faced
The data from API was quite a problem as there were many none values . Therefore, it was problematic to do bigger analysis.


## Conclusion and further improvement of monitoring.
 The use of real-time visualization and alerting can also improve communication and coordination between different stakeholders, reducing the impact of delays and disruptions. By refining and improving the platform, we can make air travel safer and more efficient.

 There are several ways to improve the monitoring of air traffic using the real-time data and analytics platform:
 Real-time Alerting, Predictive Analytics-For example, we can use machine learning models to predict which flights are likely to experience delays based on historical data, weather conditions, or other factors. This can help airlines and airports to proactively manage their operations and minimize disruptions.