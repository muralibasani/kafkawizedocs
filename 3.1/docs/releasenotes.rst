Release Notes
=============

- The below changes are part of release 5.0.3

- ACLs can be added based on Usernames (plain text principles). Ex : alice, john
    On kafka cluster, Producer acls reflects like below for user 'alice' for a topic.
    (principal=User:alice, host=*, operation=WRITE, permissionType=ALLOW)
    (principal=User:alice, host=*, operation=WRITE, permissionType=ALLOW)

-----------------------------------------------------------------------------------
- The below changes are part of release 5.0.2

- Introducing Liquibase for all database migrations
- Recaptcha validation can be disabled if running in saas mode

-----------------------------------------------------------------------------------

Kafkawize 5.0.0

Topics (approval): Create, Update, Delete, Promote
Acls (approval):  Create
Connectors (approval): Create
Avro Schemas (approval): Create
Topic Overview :
    Topic Config
    Promote
    Literal and Prefixed subscriptions
    Topic documentation
    Consumer offsets/ lag
    View topic contents
View created, completed, declined, all Topic requests
View created, completed, declined, all Acl requests
View created, completed, declined, all Connector requests
View created, completed, declined, all Avro schema requests

Synchronization from and to kafka clusters
Reconciliation and email notifications on differences between Kafkawize and Clusters
Restore configuration (topics, acls)

Login :
    Active directory integration
    Single Sign-on (OAuth2)

Clusters and Environments
    Clusters can be created connecting to Kafka clusters. (Cluster Management Api should be configured)
    Environments are wrappers over clusters, enforcing flexible configs like prefix, suffix etc

Users, Teams & Authorizations
    Configurable users, teams
    More than 35 permissions
    Configurable roles (Roles can be pulled from AD for authorization)

Topic naming conventions
    Enforce prefix and suffixes per environment

Excel report (for your team and all teams, depending on the role)
    Topics per cluster (for teams)
    Partitions per cluster
    Overall topics in all clusters
    Acls per cluster (for teams)
    Producer Acls  (for teams)
    Consumer Acls  (for teams)
    Consumer groups of all environments
    Requests per day

Analytics
    View charts of topics, partitions, acls, requests

Multi tenancy
    Each tenant can manage their topics with their own teams in isolation.
    Every tenant can have their own set of Kafka environments, and users
    of one tenant cannot view/access topics, acls or any from other tenants.
    It provides an isolation avoiding any security breach.

Kafka Connectivity
    PLAINTEXT, SSL, SASL

Audit
    All topic, acl, schema and connector requests

Email notifications when
    requests are created, approved, declined
    users are created, approved

Help Wizard to setup Kafkawize

-----------------------------------------------------------------

Kafkawize 4.5.1

Kafkawize 4.5.1 is a minor release having minor improvements

1. Updated datasource to Hikari
2. Connection parameters now have few caching related parameters for prepared statements.
3. Few code enhancements
4. Removed Cassandra datasource and related dependencies
5. Upgrade of kafka client version in cluster api to 2.6.1

----------------------------------------------------------------

Kafkawize 4.5

Kafkawize 4.5 has several changes including the below.

1. New dashboard displaying the following details
    a. My team topics
    b. My producer topics
    c. My consumer topics
    d. My team members
    e. Chart with Activity log overview of your team
    f. Chart with topics on different clusters of your team
    g. Pending Topics requests
    h. Available Clusters and their status

2. Show Producer and Consumer topics when requested from Dashboard
3. Enabled deep linking of urls
4. Color layout similar to pro version, and updated logos
5. Comma separated bootstrap servers for Kafka and schema registry clusters. (Removed explicit port field.)
6. Pagination on users page
7. Users page for a team
8. Bug fix for displaying team on Request acl page
9. Improvement on processing concurrent requests
10. Code improvisation : removed commented blocks and unused FE calls
11. Added Spring shutdown hooks and removed system exits.
12. Removed support for Cassandra metastore option.
13. Support for File based metastore (File - H2 database)
14. Upgraded Kafka client to 2.5.1
15. Database changes, following better naming conventions.

----------------------------------------------------------------

Kafkawize 4.4

1. Changes include improved User interface and few bug fixes.
2. Metadata Synchronize option has been removed
3. SSL connectivity to Kafka cluster has been removed
4. Dashboard updated to show logged in Username, Team and Role
5. Users can now only 4 environments DEV, TST, ACC and PRD. Hierarchy is defined in properties file.
6. New model for UserInfo class is introduced to fix a password bug
7. Password is not stored as encrypted text
8. Validations bug in acls and topics requests
9. Connect to Kafka clusters during start of Kafkawize

----------------------------------------------------------------

Kafkawize 4.3

Changes include improved User interface and few bug fixes.

----------------------------------------------------------------


Kafkawize 4.2

Changes include
1. Critical bug fix - concurrent user access
1. Ability to have environments DEV, TST, ACC and PRD
2. Ability to request for topics in DTAP environments
3. Ability to view topic overview and subscriptions in one page
4. Ability to view topic partitions and replication factor of all environments in topic overview page
5. Ability to view topics and their existence in all environments
6. Updated dashboard to view your team topics

----------------------------------------------------------------

Kafkawize 4.1

Changes include
1. New Bootstrap 4 User interface with new appealing look and feel
2. New UI/UX - for great user experience
3. Few bug fixes
1. Critical bug fix - concurrent user access

----------------------------------------------------------------

Kafkawize 4.0


Changes include
1. About 320 Unit tests. Above 85% code coverage.
2. Integration tests for both stores Cassandra and Rdbms, with EmbeddedCassandra and Embedded H2 sql database
3. New UI for viewing topics
4. New UI for viewing acls of topic
5. New UI for approving topics
6. New UI for approving acls
7. New UI for login screen
8. New UI for Dashboard, showing cluster api status and kafka cluster statuses
9. Added License key validation
10. Bug fixes and code enhancements

There are several other changes and upgraded dependencies which improved the code quality and efficiency.
1. New Bootstrap 4 User interface with new appealing look and feel
2. New UX - for great user experience
3. Few bug fixes


----------------------------------------------------------------

Kafkawize 3.5

Changes include
1. New page (Admin-ServerConfig) to display server configuration - application properties
2. Default replication factor, default partitions and default max partitions can be configured from Clusters page.
3. Couple of minor bug fixes
1. About 320 Unit tests. Above 85% code coverage.
2. Integration tests for both stores Cassandra and Rdbms, with EmbeddedCassandra and Embedded H2 sql database
3. New UI for viewing topics
4. New UI for viewing acls of topic
5. New UI for approving topics
6. New UI for approving acls
7. New UI for login screen
8. New UI for Dashboard, showing cluster api status and kafka cluster statuses
9. Added License key validation
10. Bug fixes and code enhancements

There are several other changes and upgraded dependencies which improved the code quality and efficiency.


----------------------------------------------------------------

Kafkawize 3.4

Changes include

1. Decline Topic requests
2. Decline Acl requests
3. Bug fix in creating topic request
1. New page (Admin-ServerConfig) to display server configuration - application properties
2. Default replication factor, default partitions and default max partitions can be configured from Clusters page.
3. Couple of minor bug fixes


----------------------------------------------------------------

Kafkawize 3.3

Changes include search features in almost all screens, bug fixes and code improvements.
Changes include
1. Decline Topic requests
2. Decline Acl requests
3. Bug fix in creating topic request

----------------------------------------------------------------

Kafkawize 3.2

Changes include search features in almost all screens, bug fixes and code improvements.

----------------------------------------------------------------

Kafkawize 3.1

New features:
1. Support for RDBMS store like MySql to store meta information. 1.0 only supports Apache Cassandra. It is one of the important feature which will support many customers who already have an SQL based solution.
Changing property db.storetype=rdbms/cassandra will make the difference.

Bug fixes:

There are few bugs which are fixed in Topic requests, acls and schema registry modules.

Changes include search features in almost all screens, bug fixes and code improvements.

----------------------------------------------------------------

Kafkawize 2.0

Kafkawize is a Kafka Topic management tool (A Web application) which automates the process of creating and browsing Kafka components, by introducing  roles/authorizations to users of various teams of an organization

Changes include new feature Rdbms support for metastore, package restructuring, jpa/hibernate implementation, improved code quality and bug fixes.

New features:
1. Support for RDBMS store like MySql to store meta information. 1.0 only supports Apache Cassandra. It is one of the important feature which will support many customers who already have an SQL based solution.
Changing property db.storetype=rdbms/cassandra will make the difference.

Bug fixes:

There are few bugs which are fixed in Topic requests, acls and schema registry modules.
