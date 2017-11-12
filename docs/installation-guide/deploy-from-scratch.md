## Deploy from scratch

### Installation options

Link to **standalone version** : Wildfly 10.1 configuration for Opencell v 4.7.1

Link to **cluster version** : Wildfly 10.1 config for Opencell 4 7 1 in cluster

### Step-by-step process

Steps when using our pre-packaged version of Wildfly :

1. On a Linux server (with distribution of your choice, but we prefer Debian or Ubuntu server), download the pre-packaged Wildfly 10.1 archive using the following link: 
[]()http://dl.opencellsoft.com/jbossWildflyKeycloak.zip (180Mo)

2. Unzip the file `jbossWildflyKeycloak.zip`

3. Move Jboss directory in the archive into the system /opt/ 

*	If necessary, Jboss may be located in another directory, but then it should change the way the property providers.rootDir of wildfly/standalone/configuration/meveo-admin.properties configuration file and startup script path)*

4. Install Postgresql in version 9.3 or higher (install on the same server as jboss is recommended) or Mariadb 10 or higher .

5. Create a Postgres user named opencell_db_user with password: opencell_db_password

6. Create a database named opencell_db and grant user opencell_db_user to all privileges on this database.

7. With the opencell_db_user import in opencell_db the initial datas import-postgres.sql that you can get from http://dl.opencellsoft.com/current/import-postgres.sql

8. Create a postgres user named keyclaok with password: keyclaok

9. Create a database named keycloak and grant user keycloak to all privileges on this database.

	*NB/ You can use other credentials and/or install prostgresql or mariadb on another server but you need to configure wildfly/standalone/configuration/standalone.xml with new credentials*

10. Download war application from http://dl.opencellsoft.com/current/opencell.war and put it in wildfly/standalone/deployement dir

11. Install Oracle JVM in version 8 and make it the default Java version

12. Start Wildfly application server with script located in /opt/jboss/start-opencell.sh 

	*It can be launched with a specific user but it must have the rights of access, read and write all files and subdirectories of the directory wildfly installation, advised: /opt/jboss)*