# Medical_Data_Prediction
Take a look at the Slide presentation for Details on the project.

https://drive.google.com/file/d/19j-5YscV5qmp9l_5eD-y_58dpJ9quXn_/view?usp=sharing


TABLE OF CONTENTS
- Project Overview
- Project Goals -
- Architectural Diagram
- Software Components used
- REST API -
- Rabbit MQ -
- Redis -
- Worker
- Google Auto ML
- Cloud functions
- Google Kubernetes Engine (GKE)
- Explains the capabilities and limits of your final solution
- Description
- Working -
- Using REST api to consume data from frontend/Postman.
- Debugging
- Training & Testing


## Project Overview 
The recent pandemic has raised alarms to focus on one of the most important aspects of development - Health Care Management. While health care data has various uses we are focusing on observing and predicting one of the critical parameters - patients length of stay. 
This parameter helps hospitals to identify patients who will stay longer at the time of admission .  This helps in logistics such as resource allocation. The task is to accurately predict the length of stay for each patient case by case so that hospitals can use this information for optimal resource allocation and better functioning. 
The data contains 18 parameters, some of the relates of the patient such as age, severity of illness, department, type of admission  and some other information related to location such as city, hospital region and hospital type etc.
The project goal is to build an end to end application that ingests tabular data and uses Google auto ML platform to train a model and then run predictive analysis on new data incoming data. We are trying to replicate a production level architecture using kubernetes, messaging queue, cloud function, data storages and autoML tools.
## Project Goals - 
In this project, we are trying to develop an application whose architecture replicates a real-world application with high transactions per second (Tps) and how to distribute the load uniformly across components. We are using the Google Kubernetes cluster, which is reliable and fault-tolerant towards node failures and has the auto-restart capability. Using a messaging queue to process the load without waiting for acknowledgment and also the separation of concern. Google cloud function is a lightweight pod that is activated on an event and shut down on completion of its task. 
Finally using AutoML, we are first trying to use cloud capability to perform heavy ML tasks like training models and later making predictions on the top of it. 
The cloud technologies used are -
 RPC / API interfaces ( Rest API )
Messaging  queues ( RabbitMQ)
Databases ( Redis)
Virtual Machines, containers or "functions as a service"
Cloud function 
