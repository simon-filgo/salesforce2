# API Strategy

## Objectives
- Develop a set of API to simplify the integration of salesforce with 3rd party systems
- Provide mechanism to monitor API and alert in case of issues
- Provide mechanism for error handling

## Strategy
- Provide an API to create, update and read majjor salesforce objects
- Use standardized schema for data when possible based on [schema.org](https://schema.org/), doing the translation from salesforce to schema.org in the api.

## Overview

<img width="826" alt="Screen Shot 2022-03-29 at 1 56 35 PM" src="https://user-images.githubusercontent.com/102594797/160675083-8684016a-f342-45f7-b2dd-67796020a424.png">

## Approach

### Phase 1. Base APIs
Develop the following 4 APIs for each of the base objects:

#### Naming convention:
- system_entity_action_version
- example: sf2_account_get_v1

#### Actions:
- post: post schema.org object to salesforce object and return salesforce record id
- get: retrieve salesforce object based on id or criteria and return schema.org object
- get_callback: record callback url and push new é updated salesforce records to callback url in schema.org schema
- get_bus: same as get_callback but sends to relevant BUS account instead of callback url

#### Objects:
- Accounts
- Contacts
- Products
- Pricebooks
- Pricebooks entries
- Opportunity
- Opportunity product
- Quote
- Quote line
- Order
- Order line
- Work order
- Work order line
- Service appointment



### Phase 2. Compound API
API that can handle multiple records creation at once. For example, an order object that would create account, contact, order and order lines.

