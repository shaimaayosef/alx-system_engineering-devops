 # Distributed web infrastructure
<picture>
 <img alt="task0" src="https://i.imgur.com/ti4QcyL.png">
</picture>

 ## Servers:

Server 1: Web server (Nginx)
Server 2: Application server
 ## Load Balancer:

We'll use HAProxy as the load balancer to distribute incoming traffic among the two servers.
HAProxy will be configured with a round-robin distribution algorithm, which distributes incoming requests equally among the available servers. This ensures better utilization of resources and prevents overload on any single server.
 ## Application Files:

The code base of the website www.foobar.com will be deployed on the Application Server. This includes all HTML, CSS, JavaScript, and any server-side code like PHP, Python, etc.
 ## Database:

MySQL will be used as the database.
We'll set up a Primary-Replica (Master-Slave) cluster for high availability and fault tolerance.
 ## Explanation:

 ## Load Balancer: Added to distribute incoming traffic evenly across multiple servers, improving performance and reliability.
Distribution Algorithm: Round-robin is chosen for its simplicity and fairness in distributing requests.
Primary-Replica Cluster: Implemented to ensure data redundancy, fault tolerance, and high availability of the database.
 ## Active-Active vs. Active-Passive:

In an Active-Active setup, both servers actively handle incoming requests simultaneously. This setup increases fault tolerance and scalability.
In an Active-Passive setup, one server (active) handles incoming requests while the other (passive) remains on standby. The passive server becomes active only when the active server fails.
 ## Primary vs. Replica Node:

The Primary node in the database cluster serves as the master where all write operations occur. It's responsible for propagating changes to the Replica nodes.
Replica nodes serve read-only operations and are synchronized with the Primary node to ensure data consistency.
