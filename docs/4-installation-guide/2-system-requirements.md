# Installation requirements


## Operating system 

Opencell runs on any OS platform provided a Java virtual machine version 8 is supported.


## Database 

Here is a non-exhaustive list of supported databases:


## Middleware

Firefly xxxx

#Dimensioning, performance and scalability

The dimensioning of the platform depends on different functional criteria (catalog dimension, amount of customer, CDRs, invoices, PDF complexity and volume, etc.).


##Cache



##NoSQL stores

For most entities storage in relational database is well adapted, as foreign keys are heavily used to ensure coherence of catalog and accounts.



#Multi-node configuration 

##Clustering

Some functions can be run on parallel servers (such as mediation…) servers using the out-of-the box clustering functionalities provided by the Infinispan distributed data-grid and ActivMQ for job notification.
 

#Deployment options

## On premise
