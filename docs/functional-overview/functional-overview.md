# Introduction

Opencell is the best fucking piece of software you've ever seen.

## Architecture

![functional overview](function.png "functional overview")

Opencell’s nucleus is a powerful and flexible rating, charging and billing engine capable of rating high volume/complex usage, recurring or one-off transactions, of charging rated transactions to postpaid or prepaid wallets in real-time and managing high volume billing runs.

## Data model


### Process overview

Multiple events imported through API or mediation (mass file processing), are transformed into EDR or usage events, that are attached to the subscription.



*Data model*
![figure 8 - data-model](data-model.png "Data model")

### Provider and seller 
 


## Modules
 

* **Marketing manager** provides marketing teams with capacity to manage products, bundles and offers from a functional point of view, define validation workflow processes and Customer care organization 
* **Reporting manager** includes a data warehouse with all relevant data for creating subscription-specific finance, marketing and operations reporting.
* **Order manager** orchestrates the ordering process with the overall enterprise process for validating and provisioning of external systems and managing subscription lifecycle.
* **Catalog manager** provides business analysts the ability to easily create and manage complex offers and expose them to CRMs, self-service portals and e-commerce systems. 
* **Finance manager** enables finance teams to manage subscription-specific revenue recognition rules, chart of accounts G/L mapping and close periods.
* **Account receivables manager** provides ability to apply cash received through batch processes, manage open balances and automate dunning processes per pre-defined rules. 
* **Payment manager** provides an interface with multiple payment and remittance gateways
* **Invoice composer** is used to compose invoices in PDF or paper format.
* **Mediation manager** is used to clean and aggregate multiple sources of transactional data using standard telco Diameter protocol.

* Our **customer care portal** provides the building blocks to manage your customers from your organizational point of view, validate or amend orders, create customers and manage your full 360° customer view.
* **Our selfcare portal** enables customers to register, subscribe to an offer, manage their contracts, see their usage, bills and subscribe to new options…

* CRM and e-commerce solutions such as Salesforce or Dynamics CRM or Magento,
* Business intelligence packages such as PowerBI, Qlikview, Jasper Reports or Pentaho, 
* ERP solutions such as Dynamics NAV, SAP, Sage or Odoo, 
* Payment gateways such as Ingenico, Braintree, Stripe or Slimpay
* Invoice composition tools such as Jasper Reports
* Telco-grade operating system solutions (OSS) such as Metaswitch.

## Key functions and capabilities

### Core rating, charging and billing engine


* Recurring job for recurring event rating
* Usage rating job for EDR processing and generation of wallet operations



 














* Global invoicing: This batch mode processes all billing accounts attached to a billing cycle. It is possible to select invoices by date range and choose a long or short invoicing process (with or without post invoicing report).
* Exceptional invoicing: This mode makes it possible to process specific billing accounts by selecting them manually.


During this preparation process, a billing account can be excluded if an anomaly is detected so that it can be managed in a separate dedicated bill run.
* Invoice number
* Invoice date
* Due date
* Payment method
* Amounts (amount without tax, tax amount, amount with tax)
* Net to pay




