# Pricing algorithm

# Overview
The pricing algorithm is a custom development to accomodate the different types of pricing structure. 

# Pricing structures
We support various pricing structures.
- List price based
  - list price - discount ($10 - 10% = $9)
  - list price - fixed discount ($10 - $0.90 = $9.10)
- Cost plus based
  - cost + markup ($5 + 20% = $6)
  - cost + fixed markup ($5 + $0.90 = $5.90)
  
  
## Pricing dimensions
The dimensions that affect pricing are:
- Client based:
  - Client type (distributor, reseller, industrial, commercial, consumer)
  - Client headquarter region (laurentide, lanaudiere, beauce)
  - Key client (a client considered key to Filgo)
  - Specific client (a client with a custom discount, contract, agreement)
- Geography based:
  - Delivery region (laurentide, lanaudiere, beauce)
- Product based:
  - Product type (energy, service)
  - Product category
  - Product family 
  - Product (propane, fireplace installation)


## Algorithm
The algorithm applies pricing rules from the most specific to the least specific for each dimensions





