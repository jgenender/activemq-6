Starting The Server
===================

Standalone ActiveMQ
===================

To run a stand-alone server, open up a shell or command prompt and
navigate into the `bin` directory. Then execute `./activemq run` (or
`./activemq.cmd run` on Windows) and you should see the following output

             bin$ ./activemq run

             11:05:06,589 INFO  [org.apache.activemq.integration.bootstrap] AMQ101000: Starting ActiveMQ Server
             ...
             11:05:10,848 INFO  [org.apache.activemq.core.server] AMQ221001: ActiveMQ Server version 2.5.0.SNAPSHOT (Wild Hornet, 125) [e32ae252-52ee-11e4-a716-7785dc3013a3]
          

ActiveMQ is now running.

Both the run and the stop scripts use the config under
`config/non-clustered` by default. The configuration can be changed by
running `./activemq run xml:../config/non-clustered/bootstrap.xml` or
another config of your choosing.

The server can be stopped by running `./activemq stop`

ActiveMQ In Wildfly
===================

ActiveMQ is the Default Messaging Provider in the [Wildfly Application
Server](http://www.wildfly.org/) To run the server you need to run the
standalone-full.xml configuration by running the command
'./standalone.sh -c standalone-full.xml'. You will see something like:/

            bin$ ./standalone.sh -c standalone-full.xml
              =========================================================================

              JBoss Bootstrap Environment

              JBOSS_HOME: /home/andy/projects/wildfly/build/target/wildfly-8.0.0.Beta1-SNAPSHOT

              JAVA: java

              JAVA_OPTS:  -server -XX:+UseCompressedOops -Xms64m -Xmx512m -XX:MaxPermSize=256m -Djava.net.preferIPv4Stack=true -Djboss.modules.system.pkgs=org.jboss.byteman -Djava.awt.headless=true

              =========================================================================

              14:47:33,642 INFO  [org.jboss.modules] (main) JBoss Modules version 1.3.0.Final
              14:47:34,780 INFO  [org.jboss.msc] (main) JBoss MSC version 1.2.0.Beta2
              14:47:34,875 INFO  [org.jboss.as] (MSC service thread 1-6) JBAS015899: WildFly 8.0.0.Beta1-SNAPSHOT "WildFly" starting
              14:47:40,382 INFO  [org.jboss.as.server] (Controller Boot Thread) JBAS015888: Creating http management service using socket-binding (management-http)
              14:47:40,383 INFO  [org.xnio] (MSC service thread 1-15) XNIO version 3.1.0.CR7
              14:47:40,402 INFO  [org.xnio.nio] (MSC service thread 1-15) XNIO NIO Implementation Version 3.1.0.CR7
              14:47:40,488 INFO  [org.jboss.remoting] (MSC service thread 1-15) JBoss Remoting version 4.0.0.Beta1
              14:47:40,547 INFO  [org.jboss.as.clustering.infinispan] (ServerService Thread Pool -- 36) JBAS010280: Activating Infinispan subsystem.
              14:47:40,560 INFO  [org.jboss.as.naming] (ServerService Thread Pool -- 47) JBAS011800: Activating Naming Subsystem
              14:47:40,560 INFO  [org.jboss.as.security] (ServerService Thread Pool -- 52) JBAS013171: Activating Security Subsystem
              14:47:40,567 INFO  [org.jboss.as.jacorb] (ServerService Thread Pool -- 37) JBAS016300: Activating JacORB Subsystem
              14:47:40,571 INFO  [org.jboss.as.jsf] (ServerService Thread Pool -- 43) JBAS012605: Activated the following JSF Implementations: [main]
              14:47:40,574 INFO  [org.jboss.as.webservices] (ServerService Thread Pool -- 56) JBAS015537: Activating WebServices Extension
              14:47:40,721 INFO  [org.jboss.as.connector.logging] (MSC service thread 1-6) JBAS010408: Starting JCA Subsystem (IronJacamar 1.1.0.Final)
              14:47:41,321 INFO  [org.jboss.as.naming] (MSC service thread 1-4) JBAS011802: Starting Naming Service
              14:47:41,323 INFO  [org.jboss.as.mail.extension] (MSC service thread 1-11) JBAS015400: Bound mail session [java:jboss/mail/Default]
              14:47:41,552 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-10) JBAS017502: Undertow 1.0.0.Beta16 starting
              14:47:41,552 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 55) JBAS017502: Undertow 1.0.0.Beta16 starting
              14:47:41,573 INFO  [org.jboss.as.security] (MSC service thread 1-6) JBAS013170: Current PicketBox version=4.0.17.SP1
              14:47:41,775 INFO  [org.jboss.as.connector.subsystems.datasources] (ServerService Thread Pool -- 31) JBAS010403: Deploying JDBC-compliant driver class org.h2.Driver (version 1.3)
              14:47:41,777 INFO  [org.jboss.as.connector.deployers.jdbc] (MSC service thread 1-16) JBAS010417: Started Driver service with driver-name = h2
              14:47:42,085 INFO  [org.wildfly.extension.undertow] (ServerService Thread Pool -- 55) JBAS017527: Creating file handler for path /home/andy/projects/wildfly/build/target/wildfly-8.0.0.Beta1-SNAPSHOT/welcome-content
              14:47:42,086 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-2) JBAS017525: Started server default-server.
              14:47:42,088 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-13) JBAS017531: Host default-host starting
              14:47:42,471 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-7) JBAS017519: Undertow HTTP listener default listening on /127.0.0.1:8080
              14:47:42,823 INFO  [org.jboss.as.server.deployment.scanner] (MSC service thread 1-10) JBAS015012: Started FileSystemDeploymentService for directory /home/andy/projects/wildfly/build/target/wildfly-8.0.0.Beta1-SNAPSHOT/standalone/deployments
              14:47:42,882 INFO  [org.jboss.as.remoting] (MSC service thread 1-16) JBAS017100: Listening on 127.0.0.1:9999
              14:47:43,037 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ221000: live server is starting with configuration ActiveMQ Configuration (clustered=false,backup=false,sharedStore=true,journalDirectory=/home/andy/projects/wildfly/build/target/wildfly-8.0.0.Beta1-SNAPSHOT/standalone/data/messagingjournal,bindingsDirectory=/home/andy/projects/wildfly/build/target/wildfly-8.0.0.Beta1-SNAPSHOT/standalone/data/messagingbindings,largeMessagesDirectory=/home/andy/projects/wildfly/build/target/wildfly-8.0.0.Beta1-SNAPSHOT/standalone/data/messaginglargemessages,pagingDirectory=/home/andy/projects/wildfly/build/target/wildfly-8.0.0.Beta1-SNAPSHOT/standalone/data/messagingpaging)
              14:47:43,062 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ221006: Waiting to obtain live lock
              14:47:43,103 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ221012: Using AIO Journal
              14:47:43,313 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ224067: Adding protocol support CORE
              14:47:43,426 INFO  [org.jboss.ws.common.management] (MSC service thread 1-3) JBWS022052: Starting JBoss Web Services - Stack CXF Server 4.2.1.Final
              14:47:43,448 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ224067: Adding protocol support AMQP
              14:47:43,451 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ224067: Adding protocol support STOMP
              14:47:43,453 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ224067: Adding protocol support STOMP_WS
              14:47:43,567 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ221034: Waiting to obtain live lock
              14:47:43,567 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ221035: Live Server Obtained live lock
              14:47:43,777 INFO  [org.jboss.as.connector.subsystems.datasources] (MSC service thread 1-8) JBAS010400: Bound data source [java:jboss/datasources/ExampleDS]
              14:47:43,781 INFO  [org.jboss.as.jacorb] (MSC service thread 1-1) JBAS016330: CORBA ORB Service started
              14:47:44,115 INFO  [org.jboss.as.jacorb] (MSC service thread 1-13) JBAS016328: CORBA Naming Service started
              14:47:44,345 INFO  [org.wildfly.extension.undertow] (MSC service thread 1-3) JBAS018210: Register web context: /activemq-server
              14:47:44,361 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ221020: Started Netty Acceptor version 3.6.6.Final-90e1eb2 127.0.0.1:5455 for CORE protocol
              14:47:44,362 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ221020: Started Netty Acceptor version 3.6.6.Final-90e1eb2 127.0.0.1:61616 for CORE protocol
              14:47:44,364 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ221020: Started Netty Acceptor version 3.6.6.Final-90e1eb2 org.apache.activemq.default.servlet:61616 for CORE protocol
              14:47:44,366 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ221007: Server is now live
              14:47:44,366 INFO  [org.apache.activemq.core.server] (ServerService Thread Pool -- 58) AMQ221001: ActiveMQ Server version 2.4.0.Beta2 (Andromedian Flyer, 123) [bcc1cd10-2bfb-11e3-ad5f-9f88840f9e1a]
              14:47:44,435 INFO  [org.jboss.as.messaging] (ServerService Thread Pool -- 58) JBAS011601: Bound messaging object to jndi name java:/ConnectionFactory
              14:47:44,437 INFO  [org.jboss.as.messaging] (ServerService Thread Pool -- 59) JBAS011601: Bound messaging object to jndi name java:jboss/exported/jms/ServletConnectionFactory
              14:47:44,439 INFO  [org.jboss.as.messaging] (ServerService Thread Pool -- 60) JBAS011601: Bound messaging object to jndi name java:jboss/exported/jms/RemoteConnectionFactory
              14:47:44,462 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-3) JBAS010406: Registered connection factory java:/JmsXA
              14:47:44,531 INFO  [org.apache.activemq.ra] (MSC service thread 1-3) ActiveMQ resource adaptor started
              14:47:44,532 INFO  [org.jboss.as.connector.services.resourceadapters.ResourceAdapterActivatorService$ResourceAdapterActivator] (MSC service thread 1-3) IJ020002: Deployed: file://RaActivatoractivemq-ra
              14:47:44,535 INFO  [org.jboss.as.connector.deployment] (MSC service thread 1-12) JBAS010401: Bound JCA ConnectionFactory [java:/JmsXA]
              14:47:44,536 INFO  [org.jboss.as.messaging] (MSC service thread 1-15) JBAS011601: Bound messaging object to jndi name java:jboss/DefaultJMSConnectionFactory
              14:47:44,719 INFO  [org.jboss.as] (Controller Boot Thread) JBAS015961: Http management interface listening on http://127.0.0.1:9990/management
              14:47:44,720 INFO  [org.jboss.as] (Controller Boot Thread) JBAS015951: Admin console listening on http://127.0.0.1:9990
              14:47:44,721 INFO  [org.jboss.as] (Controller Boot Thread) JBAS015874: WildFly 8.0.0.Beta1-SNAPSHOT "WildFly" started in 12184ms - Started 213 of 249 services (73 services are lazy, passive or on-demand)

          
