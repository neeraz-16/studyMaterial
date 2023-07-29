# old infra:
* application+DB+ Files all are in only one machine 
* client communicate with our server through ip address
* by a domain with dns serve, now first request go to DNS server and then DNS server return the IP address(Domain name revolution)
### drawbacks :
* not fault tolerant
* neither highly available
* Scalability issue
* Data durability 
### solution
* load balancer: it will send the request to our application (multiple instance) based on different algorithms like round robin
* application should store any state information(Stateless server )
* database:1 primary and 2 secondary database or master slave database
* database replica and their replication: we can have 1 primary and 2 secondary database
* read/write quorum :
* How to make database scalable: sharding database/partition 
* File system:
* distribute queue: we can use when we have brtust in request 

