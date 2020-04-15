## Subscriber
1. Get data from queue
2. Write it to DB 

Data specification:
```
GUID string | uint  - id of user 
Coin string - example ETH_0x45088E0838D1d55491ebEa1b2648f6f5F378aaF1
Price float64 - price in USD 
Condition bool - if above price is true
```

## Notifier 
Do all that operations each N seconds
1. Get all the Coins that needs to be fetched ﻿
2. Fetch coins from Redis / DB
3. Find all GUIDs with suitable price  ﻿ 
4. Delete them from DB
5. Send to notifier
