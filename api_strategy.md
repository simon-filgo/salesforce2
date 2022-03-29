# API Strategy

## Objectives
- Develop a set of API to simplify the integration of salesforce with 3rd party systems
- Provide mechanism to monitor API and alert in case of issues
- Provide mechanism for error handling

## Strategy
- Provide an API to create, update and read majjor salesforce objects


## Approach

### Phase 1. Base APIs
Develop the following APIs:
- process: 3.5.2.5	Manage customer master data
  - Create / update account
  - Create / update contact
  - Create / update asset
- process: 3.5.3	Develop and manage sales proposals, bids, and quotes
  - Create / update opportunity
  - Create / update quote
- process 3.5.4	Manage sales orders
  - Create / update order
- process: 5.3.1.7 Plan for service delivery
  - Create / update work orders
  - Create / update service appointments

### Phase 2. Compound APIs
