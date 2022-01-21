# Nginx - Why and How
**Why Nginx is the talk?:**

* C10k problem - The C10k problem is the problem of optimizing network sockets to handle a large number of clients at the same time [^1]
  * Today is no limit on the number of connections that are being made within the network. To overcome this problem, NGINX was introduced with an **event-driven** and **asynchronous architecture**.

* Traditional process-driven-architecture
  * Earlier, each client request was handled as an individual thread, which becomes complicated to handle the increasing connections. This leads to a delayed response, and the web server slows down. Switching between different threads requires CPU utilization along with extended memory usage and CPU time, which in turn impacts the performance of the website. With NGINX, you can get ten times better performance along with better resource utilization.
 
* Ensure the smooth flow of network traffic between clients and servers as a **Reverse Proxy Server**.[^2]
  * **Load balancing** - A reverse proxy server can act as a “traffic cop,” sitting in front of your backend servers and distributing client requests across a group of servers in a manner that maximizes speed and capacity utilization while ensuring no one server is overloaded, which can degrade performance. If a server goes down, the load balancer redirects traffic to the remaining online servers.
  * **Web acceleration** - Reverse proxies can compress inbound and outbound data, as well as **cache** commonly requested content, both of which speed up the flow of traffic between clients and servers. They can also perform additional tasks such as **SSL encryption** to take load off of your web servers, thereby boosting their performance.
  * **Security and anonymity** - By intercepting requests headed for your backend servers, a reverse proxy server protects their identities and acts as an additional defense against security attacks. It also ensures that multiple servers can be accessed from a single record locator or URL regardless of the structure of your local area network. 

**What is Nginx?**
* NGINX is a web server but commonly used as a reverse proxy. It can be scaled efficiently as a web server as well as a reverse proxy. It does not allow you to allocate a process to a particular connection, but it creates a process pool that can be easily shared among multiple connections within the network. Whenever a request is made, a resource will be allocated to the process resulting in better resource utilization that can easily handle extensive connections.



[^1]: https://en.wikipedia.org/wiki/C10k_problem
[^2]: https://www.nginx.com/resources/glossary/reverse-proxy-server/