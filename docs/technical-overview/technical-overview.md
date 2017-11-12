# Introduction

## Third party software

Opencell uses the following open source technologies and components

* Technologies
&nbsp Java Enterprise Edition 8 and JavaServer Faces (JSF) 
&nbsp Primefaces (Apache 2.0)
&nbsp Joda Time (Apache 2.0)
&nbsp Jackson 2.1.4 (Apache 2.0)
&nbsp Xalan 2.7 (Apache 2.0)
&nbsp Jasper Reports library (LGPL)

* Development tools
&nbsp Eclipse

* Servers
&nbsp JBoss EAP7 and Wildfly (including Infinispan, ActivMQ and Keycloak)

## Security, access and SSO

### Users, roles and permissions

By default, users have roles and permissions stored in database, and permissions are used throughout the services and UI layers to authorize access.

A permission entity consists in a permission action (read, update, delete…) and a resource (invoice, account…).
The association between users and permission is not done directly at the user level but through a list of roles that are themselves a list of permissions. 

A user is characterized by a unique username (unique among all providers), a password, a list of roles and a list of providers. When logged in, a user associated with several providers will be prompted to choose one provider in his web session.

### Identity and access management

Keycloak is an open source identity and access management solution aimed at modern applications and services. It makes it easy to secure applications and services with little to no code.

Opencell uses Keycloak to provide:
* Single-sign-on 
* Identity brokering and social login
* User federation
* Standard protocols (Oauth2, SAML, OpenID)
* Authorization services
* Multi-LDAP integration

### Providers and multi-tenancy

KOpencell is multi-tenant physically. Each tenant running a schema and instance in a JBOSS or on another image (VM, Docker…) is physically separated from all other tenants present on the Opencell instance. 
Providers are entities selling services to their customers, potentially through a network of resellers. Since all entities in Opencell, from catalog to accounts, are associated to a unique provider, the same JBOSS instance can host multiple Opencell instance with their providers: their data will be completely separated from the data of the other providers.



