# Nginx - Why and How
**Why :**

* C10k problem

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The C10k problem is the problem of optimizing network sockets to handle a large number of clients at the same time [^1]

* Traditional process-driven-architecture

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Earlier, each client request was handled as an individual thread, which becomes complicated to handle the increasing connections. This leads to a delayed response, and the web server slows down. Switching between different threads requires CPU utilization along with extended memory usage and CPU time, which in turn impacts the performance of the website. With NGINX, you can get ten times better performance along with better resource utilization.


[^1]: This is the first footnote.