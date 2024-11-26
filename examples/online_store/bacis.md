# Online Store
## Scope
1) store, not marketplace
2) delivery, logistic, warehouse not included

## Functional requirements:
1) main page
2) search product
3) viewing product
4) shopping cart, wishlist, payment
5) order management

# Non-functional requirements
1) Responsiveness - response time
2) High availability
3) Consistency

## Capacity estimation
### Traffic
1) MAU = 100M
2) DAU = 10M
3) 100M goods
4) 100 images views per active user daily
5) 1 order per active user

### Load
1) RPS-read: 10'000'000 * 100 / 86'400 = 11'574 ~ 10'000 RPS
2) RPS-write: 10'000 RPS / 100 = 100 RPS

### Network
image default size = 500 KB
1) Throughput: 10'000 * 500 = 5'000'000 KB/s = 5 GB/s
2) Total: 5 GB/s * 86'400 s * 365 d = 157'680'000 GB = 150-200 PB

### Storage
by default product has 10 images
1) Total: 100'000'000 * 10 * 500 KB = 500'000'000'000 KB = 500 PB
add 20% = 600 TB

### Hardware
1) Load: 10'000 RPS read / 1k RPS = 10 instances
2) Network: 5 GB/s / 0.1 GB/s = 50 instances
3) Storage: 600 PB / 8 TB = 75 instances ~ 100 instances

### Pricing
1) Network: 0.1$/GB * 200'000'000 GB = $20M
2) Storage: 600 TB * 300$ = $180'000

