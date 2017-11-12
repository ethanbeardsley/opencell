##Basic installation procedures

After installing Docker and `docker-compose`, deploy a full try environnent with Core + Selfcare + Customercare in seconds on Linux or Mac using this command:

> `curl https://docker.opencellsoft.com/deploy-opencell-try.sh | bash`

You can find more informations on : http://docker.opencellsoft.com/

##Additional docker.compose variables

Here is list of optional docker-compose variables with default values that can be used:

**Basic options**

> OPENCELL_VERSION : Version number of opencell war to auto-download it, if not present. For exemple: 4.7.1 Default value is set to last stable version.

> DB_HOST: Hostname for opencell database, by default : postgres
> DB_PORT: TCP port of database, by default : 5432
> DB_TYPE: Database type (postgresql, mariadb), by default : postgresql
> DB_DRIVER: Wildfly driver, by default : org.postgresql.Driver or org.mariadb.jdbc.Driver for mariadb
> DB_NAME: Database name, by default : opencell_db
> DB_USER: User required for database connexion, by default : opencell_db_user
> DB_PASSWORD: Password of user required for database connexion, by default : opencell_db_password

> KEYCLOAK_DB_HOST: Hostname for keycloak database, by default : postgres
> KEYCLOAK_DB_PORT: TCP port of keycloak database, by default : 5432
> KEYCLOAK_DB_TYPE: Database type (postgresql, mariadb), by default : postgresql
> KEYCLOAK_DB_DRIVER: Wildfly driver, by default : org.postgresql.Driver or org.mariadb.jdbc.Driver for mariadb
> KEYCLOAK_DB_NAME: Database name, by default : keycloak
> KEYCLOAK_DB_USER: User required for database connexion, by default : keycloak
> KEYCLOAK_DB_PASSWORD: Password of user required for database connexion, by default : keycloak
> KEYCLOAK_URL: URL used by keycloak to redirect final client and to communicate with wildfly, by default : http://localhost:8080/auth
> KEYCLOAK_REALM: Opencell's keycloak realm, by default : opencell
> KEYCLOAK_CLIENT: Opencell's keycloak client, by default : opencell-web
> KEYCLOAK_SECRET: Opencell's keycloak client secret, by default : afe07e5a-68cb-4fb0-8b75-5b6053b07dc3
> KEYCLOAK_SSL: HTTPS configuration, by default : none, other values : external, all
> KEYCLOAK_BASIC_AUTH: Boolean to allow or not basic auth, by default : true

> WILDFLY_BIND_ADDR: Wildfly bind address, by default : 0.0.0.0
> WILDFLY_MANAGEMENT_BIND_ADDR: Wildfly management bind address, by default : fisrt docker internal ip
> WILDFLY_PRIVATE_BIND_ADDR: Wildfly management bind address, by default : fisrt docker internal ip
> WILDFLY_CLUSTER_PASSWORD: Wildfly activemq password, by default : opencell
> WILDFLY_LANGUAGE: Wildfly language, by default : fr
> WILDFLY_COUNTRY: Wildfly country, by default : FR
> WILDFLY_TIMEZONE: Wildfly timezone, by default : UTC
> WILDFLY_NODE_NAME: Wildfly node name (used for cluster), by default : opencell-"a random number" 

> SMTP_HOST: Hostname or IP of SMTP server, by default : localhost
> SMTP_PORT: Port of SMTP server, by default : 465
> SMTP_FROM: Email address of the sender of the messages, by default : no-reply@my-company.com
> SMTP_USERNAME: Username for SMTP auth, by default : username
> SMTP_PASSWORD: Username password for SMTP auth, by default : password

> OPENCELL_LOG_LEVEL: Log level for org.meveo, by default : OFF
> OPENCELL_DEBUG_LEVEL: Log level for generation of opencell-debug.log file, by default : OFF
> HIBERNATE_SQL_LEVEL: Log level for org.hibernate.SQL, by default : OFF

> Other usable values : "ALL","CONFIG","DEBUG","ERROR","FATAL","FINE","FINER","FINEST","INFO","OFF","TRACE","WARN","WARNING"
HIBERNATE_SHOW_SQL: Boolean to translate HSQL to SQL, by default : false

> APP_CLUSTER: If set to "true", will use standelone-ha.xml 
> MODCLUSTER_ADVERTISE: Boolean to use advertise functionality of Apache modcluster, by default : true
> MODCLUSTER_STICKY_SESSION: Boolean to enable or disable sticky session, by default : true
> MODCLUSTER_HOST: Hotsname of Apache server, by default : modcluster
> MODCLUSTER_PORT: TCP port of Apache HTTPD server, by default : 80
> JGROUPS_EXTERNAL_ADDRESS: When use JGROUPS over TCP can specify externial IP of Wildfly, by default : get ip from ipecho.net
> JGROUPS_TCP_EXTERNAL_PORT: When use JGROUPS over TCP can specify external port, by default : 7600
> JGROUPS_TCP_BIND_PORT: When use JGROUPS over TCP, can specify bind port, by default : 7600

**Experimental values**

> MODE: ! Experimental use only ! if set to "h2" will use H2 DS for opencell and keycloak
> DISABLE_LOGGING: For totaly disable logging functionalty
> KEYCLOAK_NOT_IMPORT : If set, will not import Keycloak default datas 

