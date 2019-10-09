
Step 1:
Create Datbase first with name Camunda
This is sql File for Create Database
in sql.zip
Step 2:
- Copy file sqljdbc4-2.0.jar Into folder apache-tomcat/lib    for add library file

- Copy server config server.xml like this
Configuration to connect SQL server
<Resource name="jdbc/ProcessEngine"
              auth="Container"
              type="javax.sql.DataSource" 
              factory="org.apache.tomcat.jdbc.pool.DataSourceFactory"
              uniqueResourceName="process-engine"
              driverClassName="com.microsoft.sqlserver.jdbc.SQLServerDriver" 
              url="jdbc:sqlserver://localhost:1433;databaseName=Camunda;MVCC=TRUE;TRACE_LEVEL_FILE=0;DB_CLOSE_ON_EXIT=FALSE"
              defaultTransactionIsolation="READ_COMMITTED"
              username="sa"  
              password="@Sql2016"
              maxActive="20"
              minIdle="5"
              maxIdle="20" />


Please pay attention with port 1433