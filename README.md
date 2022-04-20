# salesforce2
Project site for salesforce2 project @ Filgo. 

## Key resources
- [Salesforce instance](https://filgosonic.my.salesforce.com/)
- [Project plan](https://app.smartsheet.com/b/publish?EQBCT=6f98c0152aa34af9975130359a2ae7be)
- [Postman API](https://go.postman.co/workspace/Filgo-Sonic~5e6ec737-1640-4f82-a0ca-ffcf61aad135/collection/5957859-76dfea71-e159-477b-b9c2-313f7107823e?action=share&creator=19922079)


## Overview
Filgo deployed Salesforce in 2020 and SFS in 2022 to support the order to cash process and field service process. 
The deployment was heavily customized and didn't use the standard salesforce objects, forcing the organization to start over. 

The project aims to rebuild salesforce properly in a new instance, minimizing customizations.  

Filgo provides energy products in eastern Canada. 

Main offerings:
- Fuel distribution
- Propane distribution
- Tanks installation and maintenance (fuel and propane)
- Heating system installation and maintenance
- Lubricant distribution
- Lubricant retail shops


## Objectives
- Setup a new salesforce instance to replace the current salesforce installation that was too heavily customized
- Allow anyone from outside the organization to quickly be able to work
- Improve performance of the lead-to-quote and quote-to-cash process 

## Strategies
- Avoid customizations, leverage built-ins funcitonalities
- Use native salesforce data model
- Enable quote to cash with a minimum of human interaction

## Key requirements
- Language and currency:
  - Multilingual screen (french and english)
  - Multilingual client documents (quotes, service reports, invoices, etc). 
  - Multicurrency (CAD as default, USD)
- Pricing:
  - Allow cost plus percentage pricing
  - Allow cost plus fixed amount pricing
  - Allow price - discount
  - Allow price - fixed amount
  - Allow volume pricing
  - Allow regional discounts (territory)
  - Allow client discounts
  - Allow client pricing agreements

## Project phases
### Phase 1. Base configuration
Configure the system with the basics.
- Company specifics
- Groups and security
- SSO
- Products
- APIs

### Phase 2. Proof of concept lubricant
Develop a proof of concept for the sales and distribution of lubricants

### Phase 3. Proof of concept service
Develop a proof of concept for field services

