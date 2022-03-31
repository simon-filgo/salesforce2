# Pricing algorithm

# Overview
The pricing algorithm is a custom development to accomodate the different types of pricing structure. 

# Pricing structures
## Summary
We support various pricing structures.
- List price based
  - list price - discount ($10 - 10% = $9)
  - list price - fixed discount ($10 - $0.90 = $9.10)
- Cost plus based
  - cost + markup ($5 + 20% = $6)
  - cost + fixed markup ($5 + $0.90 = $5.90)
  
  
## Pricing dimensions
Several dimension will affect pricing, providing additional rebate or discount. 
The dimensions that affect pricing are:
- Client based:
  - Client type (distributor, reseller, industrial, commercial, consumer)
  - Client headquarter region (laurentide, lanaudiere, beauce)
  - Key client (a client considered key to Filgo)
  - Specific client (a client with a custom discount, contract, agreement)
- Geography based:
  - Delivery country
  - Delivery region (laurentide, lanaudiere, beauce)
  - Delivery city
  - Delivery site (specific address)
- Product based:
  - Product type (energy, service)
  - Product category
  - Product family 
  - Product (propane, fireplace installation)
- quantity based:
  - quantity interval

# Pricing engine

## Pricing rules
Pricing rules are stored in a table with the schema described below. Rules can be very generic and apply to all products or all of certain tyope of clients, or very specific to a given product and client. 
Most of the fields of a pricing rules are meant to be empty. 
### Schema
- Pricing rules
  - product_type
  - product_category
  - product_family
  - product
  - client_type
  - client_category
  - client_family
  - client_tag
  - client
  - delivery_country
  - delivery_province
  - delivery_region
  - delivery_city
  - delivery_site
  - quantity_min
  - quantity_max
  - cost_override
  - list_price_override
  - discount_variable
  - discount_fixed
  - markup_variable
  - markup_fixed


### Examples of pricing rules
#### General discount for a given client 
- client: Microsoft
- discount_variable: 10%

#### General discount for a given type 
- client_type: Distributor
- discount_variable: 10%

#### Fixed amount discount for a given type 
- client_type: Distributor
- discount_fixed: $0.10

#### Volume discount for a given product if between 100 to 200
- product: Propane
- quantity_min: 100
- quantity_max: 200
- discount_variable: $0.10

## Guidelines
- Apply all available rules from most specific to least specific. 
- Don't apply two rules for the same dimension (specific product and product family for example)
- Most specific rule wins

## Algorithm
The algorithm applies pricing rules from the most specific to the least specific for each dimensions

- Step 1. Find applicable rules
  -  Find all rules applicable, from the most specific to the least specific
  -  Keep only the most specific rule for each dimension
- Step 2. Apply rules to calculate price
- Step 3. Add rules used to quotation line (???) for traceability

## Example
The following examples use the following rules as base

|Rule number |product_type |product | client_type | client |  delivery_region | delivery_site | quantity_min | quantity_max | markup_variable | markup_fixed |
|:------      |: --     |: --       |:--            |:--              |:--            |:--          |:--            |-::              |:--           |:-- |
|1            |propane     | | | | | | | |a |    }




### Scenario 1. Product specific pricing for a specific client

- Rules:
  -  


