# API Gateway
An API Gateway is a software pattern that sits in front of an application programming interface (API) or group of microservices, to facilitate requests and delivery of data and services. 

API Gateway is used to separate the client interface from the backend implementation so that the clients have a simple and dependendable experience regardless of the complexity.

## Uses of API Gateway
- Protecting your API from overuse and misuse
- Understanding how individuals are using your API
- Provide mobile clients with an endpoint to retrieve all product details with a single request
- Monetizing an API
- Adding new API services and replacing others while keeping existing services in the same place. 

## Drawbacks
- Another system that must be developed, deployed and managed. 
- Increases complexity
- Learning curve
- Response time could be slower due to the additional movement through the Gateway

## Kong
- Nginx Proxy with additional features.
- Endpoints have a 1:1 relationship with backends.
- Cannot aggregate data from several backends into one single endpoint. 
- Stateful. Configurations are stored in the database. 
- Extensions are build using Lua Plugins.

## KrackenD (Lura)
- Gateway with aggregation. KrackenD connects a lot of backend services to a single endpoint.
- Great fit for Mobile Applications.
- Stateless. There is no need for a centralized database. Nodes need not communicate with each other.
- Extensions are build using Go, Lua, etc., 

## Comparison

| Kong  | KrackenD  |
| ------------ | ------------ |
|   Stateful |Stateless |
|   Proxy with cross-cutting concerns|Not a Proxy, although it can be used as one   |
|   Nodes require coordination and synchronization|No coordination and synchronization is required   |
|   Mutable Configuration| Declarative Configuration   |
|   Configurations are stored in Database| Configurations are versioned using Source Control tools like Git.  |
|   Complex Architecture | Docker Container with Configuration File  |
|   Requires Powerful hardware to run| Runs on small and micro machines in Production  |
|   Multi-region lag (Latency)| No challenges for Multi-Region  |
|   Build extensions through Lua Plug-ins| Extensions are build in Go, Lua, etc.,  |


