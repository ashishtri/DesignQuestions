**load balancer:**
In a system, a server has a certain amount of capacity to handle the load or request from users. If a server receives a lot of requests simultaneously more than it’s capacity than the throughput of the server gets reduced and it can slow down. Also, it can be failed (no availability) if it continues for a longer period. You can add more servers (**horizontal scaling)** and resolve this issue by distributing the number of requests among these servers. Now the question is who is going to take ownership of distributing the request and balancing the load. Who is going to decide which request should be allocated to which server to ease the burden of a single server? Here comes the role of the load balancer. 

A load balancer’s job is to distribute traffic to many different servers to help with **throughput, performance, latency, and scalability.** You can put the load balancer in front of the clients (it can be also inserted to other places) and then the load balancer will route the incoming request across multiple web servers. In short, load balancers are traffic managers and they take responsibility for the availability and throughput of the system. Nginx, Cisco, TP-Link, Barracuda, Citrix, Elastic Load Balancing from AWS…these are some popular load balancers available in the market. 


**Caching**
usually your web server is not the first to go down, in fact, quite often is your database server which may be under high loads for lots of writes or reads operations. Quite often we hit the database for various queries and joints which slows downs the performance of the system. To handle these queries and lots of reads and write caching is the best technique to use. 
If you need to rely on a certain piece of data often then cache the data and retrieve it faster from the memory rather than disk. This process reduces the workload on the backend servers. Caching helps in reducing the-network calls to the database. Some popular caching services are Memcache, Redis, and Cassandra. A lot of websites use CDN (content delivery network) which is a global network of servers. CDN cache static assets files like images, javascript, HTML, or CSS and it makes accessing very fast for the users. 


**Proxies**
Typically proxy servers are some bit of code or intermediary piece of hardware/software that sits between a client and another server. It may reside on the user’s local computer or anywhere in between the clients and the destination servers. A proxy server receives requests from the client and transmits it to the origin servers, then it forwards the received response from the server to the originator client. In some cases, when the server receives the request the IP address is not associated with the client but it is of the proxy server. This happens when the proxy server hides the identity of the client. 
when people use the term proxy they refer to ‘forward proxy’. ‘Forward proxy’ is designed to help users and it acts on behalf of (substitute for) the client in the interaction between client and server. It forwards the user’s requests and acts as a personal representative of the user. In system, design especially in complex systems, proxies are very useful, particularly ‘reverse proxies’ are useful. ‘Reverse proxies’ are the opposite of ‘forward proxy’. A reverse proxy acts on behalf of a server and it is designed to help servers. 
In the ‘forward proxy’ server won’t know that the request and response are routed through the proxy, and in a reverse proxy, the client won’t know that the request and response are traveling through a proxy. A ‘reverse proxy’ can be assigned a lot of tasks to help the main server and it can act as a gatekeeper, a screener, a load-balancer, and an all-around assistant.

![image](https://user-images.githubusercontent.com/37074584/113472261-a4b4c580-947f-11eb-92df-3acf2393027c.png)


![image](https://user-images.githubusercontent.com/37074584/113472268-ada59700-947f-11eb-8d21-d7eaba10e7e6.png)

**CAP Theorem**
Consistency, Availability, and Partition tolerance.

The theorem states that you cannot achieve all the properties at the best level in a single database, as there are natural trade-offs between the items. You can only pick two out of three at a time and that totally depends on your prioritize based on your requirements.


![image](https://user-images.githubusercontent.com/37074584/113472343-489e7100-9480-11eb-9183-70868ca832f3.png)


**Consistency** means that any read request will return the most recent write. Data consistency is usually “strong” for SQL databases and for NoSQL database consistency may be anything from “eventual” to “strong”.
**Availability** means that a non-responding node must respond in a reasonable amount of time. Not every application needs to run 24/7 with 99.999% availability but most likely you will prefer a database with higher availability.
**Partition tolerance** means the system will continue to operate despite network or node failures.

CA systems are not defined for distributed systems. However, in the case of a single node setup, you can get CA capabilities. Further, distributed systems have to support partition tolerance due to network failures. Hence, either you choose Consistency or Availability i.e build a CP or an AP system.


**Databases**










