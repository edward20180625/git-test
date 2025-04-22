PS C:\Users\F2LIPBX> Test-NetConnection -ComputerName W3DVDS1051.1dc.com -Port 1433


ComputerName     : W3DVDS1051.1dc.com
RemoteAddress    : 100.64.1.65
RemotePort       : 1433
InterfaceAlias   : Wi-Fi
SourceAddress    : 192.168.1.152
TcpTestSucceeded : True



onfiguration.class]: liquibase.exception.DatabaseException: com.microsoft.sqlserver.jdbc.SQLServerException: The TCP/IP connection to the host w3dvdvds1051.1dc.com, port 1433 has failed. Error: "w3dvdvds1051.1dc.com. Verify the connection properties. Make sure that an instance of SQL Server is running on the host and accepting TCP/IP connections at the port. Make sure that TCP connections to the port are not blocked by a firewall.".
2025-04-22T13:06:54.333-05:00  INFO 13056 --- [           main] o.apache.catalina.core.StandardService   : Stopping service [Tomcat]
2025-04-22T13:06:54.480-05:00  INFO 13056 --- [           main] .s.b.a.l.ConditionEvaluationReportLogger :

Error starting ApplicationContext. To display the condition evaluation report re-run your application with 'debug' enabled.
2025-04-22T13:06:55.405-05:00 ERROR 13056 --- [           main] o.s.boot.SpringApplication               : Application run failed

org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'entityManagerFactory' defined in class path resource [org/springframework/boot/autoconfigure/orm/jpa/HibernateJpaConfiguration.class]: Failed to initialize dependency 'liquibase' of LoadTimeWeaverAware bean 'entityManagerFactory': Error creating bean with name 'liquibase' defined in class path resource [org/springframework/boot/autoconfigure/liquibase/LiquibaseAutoConfiguration$LiquibaseConfiguration.class]: liquibase.exception.DatabaseException: com.microsoft.sqlserver.jdbc.SQLServerException: The TCP/IP connection to the host w3dvdvds1051.1dc.com, port 1433 has failed. Error: "w3dvdvds1051.1dc.com. Verify the connection properties. Make sure that an instance of SQL Server is running on the host and accepting TCP/IP connections at the port. Make sure that TCP connections to the port are not blocked by a firewall.".
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:328) ~[spring-beans-6.2.3.jar:6.2.3]
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:207) ~[spring-beans-6.2.3.jar:6.2.3]
        at org.springframework.context.support.AbstractApplicationContext.finishBeanFactoryInitialization(AbstractApplicationContext.java:970) ~[spring-context-6.2.3.jar:6.2.3]
        at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:627) ~[spring-context-6.2.3.jar:6.2.3]
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:146) ~[spring-boot-3.4.3.jar:3.4.3]
        at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:752) ~[spring-boot-3.4.3.jar:3.4.3]
        at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:439) ~[spring-boot-3.4.3.jar:3.4.3]
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:318) ~[spring-boot-3.4.3.jar:3.4.3]
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:1361) ~[spring-boot-3.4.3.jar:3.4.3]
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:1350) ~[spring-boot-3.4.3.jar:3.4.3]
        at admin.RapidAdminApplication.main(RapidAdminApplication.java:10) ~[classes/:na]
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'liquibase' defined in class path resource [org/springframework/boot/autoconfigure/liquibase/LiquibaseAutoConfiguration$LiquibaseConfiguration.class]: liquibase.exception.DatabaseException: com.microsoft.sqlserver.jdbc.SQLServerException: The TCP/IP connection to the host w3dvdvds1051.1dc.com, port 1433 has failed. Error: "w3dvdvds1051.1dc.com. Verify the connection properties. Make sure that an instance of SQL Server is running on the host and accepting TCP/IP connections at the port. Make sure that TCP connections to the port are not blocked by a firewall.".
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1812) ~[spring-beans-6.2.3.jar:6.2.3]
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:601) ~[spring-beans-6.2.3.jar:6.2.3]
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:523) ~[spring-beans-6.2.3.jar:6.2.3]
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:339) ~[spring-beans-6.2.3.jar:6.2.3]
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:346) ~[spring-beans-6.2.3.jar:6.2.3]
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:337) ~[spring-beans-6.2.3.jar:6.2.3]
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202) ~[spring-beans-6.2.3.jar:6.2.3]
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:315) ~[spring-beans-6.2.3.jar:6.2.3]
        ... 10 common frames omitted
Caused by: liquibase.exception.UnexpectedLiquibaseException: liquibase.exception.DatabaseException: com.microsoft.sqlserver.jdbc.SQLServerException: The TCP/IP connection to the host w3dvdvds1051.1dc.com, port 1433 has failed. Error: "w3dvdvds1051.1dc.com. Verify the connection properties. Make sure that an instance of SQL Server is running on the host and accepting TCP/IP connections at the port. Make sure that TCP connections to the port are not blocked by a firewall.".
        at liquibase.integration.spring.SpringLiquibase.afterPropertiesSet(SpringLiquibase.java:267) ~[liquibase-core-4.29.2.jar:na]
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.invokeInitMethods(AbstractAutowireCapableBeanFactory.java:1859) ~[spring-beans-6.2.3.jar:6.2.3]
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1808) ~[spring-beans-6.2.3.jar:6.2.3]
        ... 17 common frames omitted
Caused by: liquibase.exception.DatabaseException: com.microsoft.sqlserver.jdbc.SQLServerException: The TCP/IP connection to the host w3dvdvds1051.1dc.com, port 1433 has failed. Error: "w3dvdvds1051.1dc.com. Verify the connection properties. Make sure that an instance of SQL Server is running on the host and accepting TCP/IP connections at the port. Make sure that TCP connections to the port are not blocked by a firewall.".
        at liquibase.integration.spring.SpringLiquibase.lambda$afterPropertiesSet$0(SpringLiquibase.java:259) ~[liquibase-core-4.29.2.jar:na]
        at liquibase.Scope.lambda$child$0(Scope.java:191) ~[liquibase-core-4.29.2.jar:na]
        at liquibase.Scope.child(Scope.java:200) ~[liquibase-core-4.29.2.jar:na]
        at liquibase.Scope.child(Scope.java:190) ~[liquibase-core-4.29.2.jar:na]
        at liquibase.Scope.child(Scope.java:169) ~[liquibase-core-4.29.2.jar:na]
        at liquibase.Scope.child(Scope.java:257) ~[liquibase-core-4.29.2.jar:na]
        at liquibase.integration.spring.SpringLiquibase.afterPropertiesSet(SpringLiquibase.java:250) ~[liquibase-core-4.29.2.jar:na]
        ... 19 common frames omitted
Caused by: com.microsoft.sqlserver.jdbc.SQLServerException: The TCP/IP connection to the host w3dvdvds1051.1dc.com, port 1433 has failed. Error: "w3dvdvds1051.1dc.com. Verify the connection properties. Make sure that an instance of SQL Server is running on the host and accepting TCP/IP connections at the port. Make sure that TCP connections to the port are not blocked by a firewall.".
        at com.microsoft.sqlserver.jdbc.SQLServerException.makeFromDriverError(SQLServerException.java:231) ~[mssql-jdbc-12.4.2.jre11.jar:na]
        at com.microsoft.sqlserver.jdbc.SQLServerException.convertConnectExceptionToSQLServerException(SQLServerException.java:282) ~[mssql-jdbc-12.4.2.jre11.jar:na]
        at com.microsoft.sqlserver.jdbc.SocketFinder.findSocket(IOBuffer.java:2578) ~[mssql-jdbc-12.4.2.jre11.jar:na]
        at com.microsoft.sqlserver.jdbc.TDSChannel.open(IOBuffer.java:719) ~[mssql-jdbc-12.4.2.jre11.jar:na]
        at com.microsoft.sqlserver.jdbc.SQLServerConnection.connectHelper(SQLServerConnection.java:3523) ~[mssql-jdbc-12.4.2.jre11.jar:na]
        at com.microsoft.sqlserver.jdbc.SQLServerConnection.login(SQLServerConnection.java:3172) ~[mssql-jdbc-12.4.2.jre11.jar:na]
        at com.microsoft.sqlserver.jdbc.SQLServerConnection.connectInternal(SQLServerConnection.java:3014) ~[mssql-jdbc-12.4.2.jre11.jar:na]
        at com.microsoft.sqlserver.jdbc.SQLServerConnection.connect(SQLServerConnection.java:1836) ~[mssql-jdbc-12.4.2.jre11.jar:na]
        at com.microsoft.sqlserver.jdbc.SQLServerDriver.connect(SQLServerDriver.java:1246) ~[mssql-jdbc-12.4.2.jre11.jar:na]
        at com.zaxxer.hikari.util.DriverDataSource.getConnection(DriverDataSource.java:137) ~[HikariCP-5.1.0.jar:na]
        at com.zaxxer.hikari.pool.PoolBase.newConnection(PoolBase.java:360) ~[HikariCP-5.1.0.jar:na]
        at com.zaxxer.hikari.pool.PoolBase.newPoolEntry(PoolBase.java:202) ~[HikariCP-5.1.0.jar:na]
        at com.zaxxer.hikari.pool.HikariPool.createPoolEntry(HikariPool.java:461) ~[HikariCP-5.1.0.jar:na]
        at com.zaxxer.hikari.pool.HikariPool.checkFailFast(HikariPool.java:550) ~[HikariCP-5.1.0.jar:na]
        at com.zaxxer.hikari.pool.HikariPool.<init>(HikariPool.java:98) ~[HikariCP-5.1.0.jar:na]
        at com.zaxxer.hikari.HikariDataSource.getConnection(HikariDataSource.java:111) ~[HikariCP-5.1.0.jar:na]
        at liquibase.integration.spring.SpringLiquibase.lambda$afterPropertiesSet$0(SpringLiquibase.java:254) ~[liquibase-core-4.29.2.jar:na]
        ... 25 common frames omitted


