1 QUESTION ONE  


# INTRODUCTION TO SYSTEM DESIGN  
***System design***: step by step process of defining a particular software's achitecture, modules, components etc.  
A base concept in software engineering and is vital in building scalable and reliable software. It is used to prepare architecture of software apps   
## Steps of software development  
1. Ask for requirements (Non functional or functional)  
1. System design (prepare the architecture for the app) eg whether to use SQL or NoSQL database.  
1. How to make the app scalable incase of traffic.  

## Exploring essential design methods in system design 
1. ***Architecture design***  
Describes infrastructure, model, view, components and interaction. They include client-server interaction, microservices etc.
1. ***ERD Diagram***  
Entity-relationship diagram is used for designing the app's database structure.  
1. ***UML Diagram***  
Unified modified language is used to prepare modelling software systems. It contains differnt diagrams like activity diagrams, class diagrams sequence diagrams, etc to represent the different aspects of the system.  
1. ***Class diagram***  
Used to represent classes their attributes method and relationships between multiple classes and to provide overview of the system's data and functionality.  
1. ***Sequence Diagram***  
Represents interaction between various components of the system. It is used to model the behaviour of the system.eg User Center input on the front end side of the app, how the app should process data and return the response.  

## System design concepts  
1. ***Performance vs Scalability***  
*Performance*: Time a website takes to load. Caching can be used to increase the app's performance and resources faster.  
*Scalability*: Ability to scale the app. How to handle more requests can be solved by scaling the app by distributing the load across multiple servers or increasing the single servers capacity.  
1. ***Latency vs Throughput***  
*Latency*: Measurement of the time delay to complete a single request or data operation.crucial in online or in live gaming, live streaming, video calls, etc for seamless user experience. (measured in milliseconds)   
*Throughput*: No. of operations the system can handle at a particular time or amount of data passed via a network request in a given time (measured in mb per second). Used to check capability of the systems.If the throughput of the server is low architecturees can scale the server to make  it efficient.  
1. ***Consistency Patterns vs Availability Patterns***   
*Consistency*: ensures all nodes in the system read the same data at a particular time.  
*Availability*: The system's availability ensures that each request receives a response either with fresh or old data. I mportant when high uptime is needed.  
### Consistency Patterns  
1. Strong consistency: Each request gets the most recent data. To achieve it one requires synchronised communications prioritizes consistency over availability.
  
  1. Eventual consistency: allows temporary inconsistencies to be resolved soon. Prioritizes availability over consistency.  
  1. Weak consistency: The user may get after writing the data it focuses on the fast access. It can be used in live streaming or video chat.  
  ### Availability Patterns 
  
  1. Load balancing: Up coming request can be distributed across multiple servers to achieve high availability.  
  1. Retry and timeout strategies: Mechanism to process the request after every interval if the system fails or is not available eg Refreshing a website to get a response.  
  # ADVANCED CONCEPTS IN SYSTEM DESIGN  
  1. CDN - Content delivery network. Distributed server network located at different geolocations. The CDN is used to deliver content like images, various data etc from the serve. Delivers the resource faster decreases latency (network delay) and improves the app's performance.  
  2. DNS - Domain name system allows users to access the website resources using the domain name.  
  When one makes a request for the resources of IP addresses which are mapped with the domain name.  
1. Caching - Mechanism to serve resources faster. High speed storage.Works between web apps and the source of data.  
4. Proxies - proxy  server. The proxy server works between the client of the application and the internet. It gets resources requested and sends them back to the applications.  
# COMPONENTS OF SYSTEM DESIGN  
1. ***Microservices and Service discovery***  
Microservices breakdown complex applications into small services such that each service works indepedently and accomplishes specific task. Every microservice has a unique ID and name for its identification.  
 Dynamic service discovery- each microservice can dynamically find other services located in the same network. So sacling and load balancing became easy.  
 1. ***Database systems, RDBMS and NoSQL***  
 a. RDBMS  
 Relational database management system. SQL databases are built on top of the RDBMS.  
 Used when you need to store structured data which makes it easier to access the data from the database and connect it with other data as they are stored in table format.  
 #### Characteristics of RDBMS database.  
 * Stores the data in the table format.  
 * You cant scale RDBMS database horizontally rather vertically.  
 * SQL is a query language for RDBMS database.  
 * Accessing data from the RDBMS database is slow. 

 b. ***NoSQL***  
NoSQL   dabase stores the data in the key-value pair instead of in table format.  
Used when you require to store unstructured data in the database.  
#### Characteristics of NoSQL database  
* Stores data in key value format.   
* Horizontally scalable as you can add new key value pairs for new attributes.
* Each record can contain different key-value pairs. 
* faster than RDBMS database.  
* Supports frequent changes in the databases.  

3. ***Communications protocols***  

* HTTP/HTTPS: Hyper text transfer protocol.HTTPS is a secure version of HTTP. They are used in web-based communication. It is a good idea to use HTTPS always for security reasons.  
* TCP/IP: The TCP stands for the transmission control protocol. The TCP protocol is used to communicate over the internet. eg.  it is used in the chatting application.  
*  UDP: User datagram protocol. It is mainly used for live streaming, video calls, etc., in which data loss can be tolerable.  
* WebSockets: Web sockets are used for bi-directional duplex communication. It builds the connection between two web applications.  

# STEPS OF DESIGNING A SYSTEM  
1. Requirements  
a. Function requirements: Requirements in the application with which the user interacts. For example, authentication, navigation, payment services integration, etc.  
b. Non-function requirements: Requirements to improve the application's capabilities. For example, high availability, scalability, consistency, low latency, high throughput, etc., are the non-functional requirements.  
2. Estimation of resources - 
While selecting the resources for the server, you should keep in mind how howmany requests it will receive per day or second.
Furthermore, you are also required to decide how much data you require to store in the database.  
3. System interface definition - Defining the API endpoints and what to expect from each API endpoint.  
4. Defining data model - Select a database for the application, depending on whether you want structured or unstructured data. eg while building a social media app eg FaceBook or Twitter one can use Graph Databases to manage many relationships.  
5. High-level design - Decide how you will connect the components of the system with each other. For example, connecting the server with the database, connecting the server with the client, and integrating the third-party tools with the applications.  
6. Improve the system design by analyzing the system to fulfill the non-functional requirements.
You can analyze it as given below:  
* How to use caching to improve the performance of the application?
* How do we scale the application via load balancing?
* Should you use the CDN for caching, or are cookies enough?
* How would you handle the failure of the application?
* Should you distribute the data across multiple databases?
* How will you replicate the database?  
7. Identifying and resolving bottlenecks
Identify the bottlenecks in your system design and discuss the solutions to resolve them with the interviewer.
The sample bottlenecks can be shown below.  
* Can the system fail in any scenario? If yes, how will you handle it?
* How do you monitor the performance of the system and issues in the system?
* Do you have enough replicas of the database to handle the failure?



