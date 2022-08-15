# BankingMicroservicesProject
#BankingMicroservices Includes
Microservices
Here this project consist of mainly 5 microservices and those are
1.#User service (banking-core-user-service) – This service includes all the operations under the User such as registrations and retrieval. Additionally, this API consumes keycloak REST API to register and manage the user base while using the local PostgreSQL database as well.
2. #Fund transfer service (banking-core-fund-transfer-service) – This is the service that handles all the fund transfers between accounts and this API will push messages to a centralized RabbitMQ queue to use from the Notification service.
3. #Payment service (banking-core-payments-service) – This service will include all the API endpoints to process Utility payments in this project and that will push notification messages to RabbitMQ as well.
4. #Notification service – This API is registered under the service registry but consumes all the messages from RabbitMQ and pushes necessary notifications to the end users.
5. #Banking core service – This is the banking core service that acts as a dummy banking core with accounts, users, transaction details, and processors for banking transactions.
Other components inside this architecture

1.Service Registry – For this, I’m going to use Netflix Eureka Service Registry.
2.API Gateway – Gateway will be configured using Spring cloud gateway.
3. Configuration Service – This will be deployed using Spring Cloud Config Server and Client.
4. Authentication – Here I’m using Keycloak for authentication and authorization, Keycloak is a open-source Identity management system and we could easily build user related stuff. Additionally, keycloak comes with a handy REST API that allows us to communicate as an API and get things done within seconds.
5. Database – For this tutorial will use multiple MySQL database instances.
6. Message Queues – RabbitMQ will be the main message queue supplier in this project and I’m having an idea of integrating more tools like RabbitMQ into this same project in the future.
7. Logging – ELK stack will be used to manage logs and process custom datasets for quick queries inside the architecture.
8. Server API Documentation – API documentation for microservices will be done using Swagger with UI.
9.Monitoring – Here we are using Prometheus, Micrometer, and Grafana to monitor the whole application setup after deploying into the servers.
10. Distributed tracing – Zipkin will be the tool that we are going to use with this project in order to trace whole application requests and details about the performance.
