# System Design Notes

- Single server - Single point of failure
- Always separate out the web server and database server

## Scaling
- Vertical scaling - fewer servers to maintain
- Horizontal scaling
    - Loadbalancer
    - Stateless, Any web server can handle any requests at any time
### Failover servers
- Cold standby 
    - Period backups are taken 
    - During failover, backups restored to cold standby and requests re-directed to new server
    - Advantages & disadvantages
        - *cheaper*
        - *increased downtime*
        - *dataloss during failover - any transcations happend during backup and restore*
- Warm standby
    - Continuous Replication
    - Advantages & disadvantages
        - *simple*
        - *vertical scaling*
- Hot standby
    - Replication 
- Multi primary
    - Many primary database servers

## Sharding
Hortizontal partition of databases into different servers

- MongoDB
- Cassandra - Ring

## ACID Compliance

- Atomicity
- Consistency = Correctness
- Isolation
- Durability

## CAP Theory

Consistency
Availability
Partition tolerance

## Caching

## CDN

## Resiliency 

Keep data in different rack, data center, availability zones, region etc. 
Tradeoffs - cost

## Distributed storage
- Scalable
- Highly available
- Secure
- Durable


