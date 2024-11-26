## Scope refinement

## Functional requirements

## Non-functional requirements

## Capacity estimation
### Traffic
1) MAU - monthly active users
2) DAU - daily active users
3) content per user session

### Load
1) RPS-read - Requests Per Second
2) RPS-write

AZURE default instance:
1) text data = 100k RPS
2) DB read = 10k RPS
3) DB write = 1k RPS

### Network
1) Concurrent connections
2) Network throughput - Gb/s

Specifications:
1) Cloud connections - 1 GbE; Price $0.1/GB
2) Twisted pair (Cat6a+) - 10 GbE
3) Optical fiber (QSFP+) - 40 GbE
4) InfiniBand - 100+ GbE

### Storage
1) Ingress Data
2) Egress Data
3) Data Volume

Specifications:
1) HDD - 100-300 MB/s, 20 TB, 500$
2) SSD - 3-5 GB/s, 8 TB, 2000$
3) RAM - 50 GB/s, 128 GB, 1000$

Storing 1 TB costs approximately 30$ HDD, 300$ SSD, 10'000$ RAM
Single server can hold up to 1 TB of RAM, 50 TB SSD, or 200 TB of HDD

AFR - Annualized Failure Rate ~ 1%

Single server specs:
1) load = 1k RPS
2) network = 0.1 GB/s (1Gbe - cloud)
3) storage = 8 TB