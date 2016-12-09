1) Copy the first line from your server log
```
2016-12-08 21:26:17,403 INFO main:com.cloudera.server.cmf.Main: Starting SCM Server. JVM Args: [-Dlog4j.configuration=file:/etc/cloudera-scm-server/log4j.properties, -Dfile.encoding=UTF-8, -Dcmf.root.logger=INFO,LOGFILE, -Dcmf.log.dir=/var/log/cloudera-scm-server, -Dcmf.log.file=cloudera-scm-server.log, -Dcmf.jetty.threshhold=WARN, -Dcmf.schema.dir=/usr/share/cmf/schema, -Djava.awt.headless=true, -Djava.net.preferIPv4Stack=true, -Dpython.home=/usr/share/cmf/python, -XX:+UseConcMarkSweepGC, -XX:+UseParNewGC, -XX:+HeapDumpOnOutOfMemoryError, -Xmx2G, -XX:MaxPermSize=256m, -XX:+HeapDumpOnOutOfMemoryError, -XX:HeapDumpPath=/tmp, -XX:OnOutOfMemoryError=kill -9 %p], Args: [], Version: 5.9.0 (#249 built by jenkins on 20161006-1801 git: 898a5e032c080e18833dfc58180761f6ef2ea351)

```

2) Copy the log line that contains the phrase "Started Jetty server"
```
2016-12-08 21:27:32,278 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.
```

3) Copy your db.properties file to challenges/labs/2_db.properties.md
```

[root@ip-172-31-1-155 ~]# cat /etc/cloudera-scm-server/db.properties
# Auto-generated by scm_prepare_database.sh on Thu Dec  8 21:20:56 EST 2016
#
# For information describing how to configure the Cloudera Manager Server
# to connect to databases, see the "Cloudera Manager Installation Guide."
#
com.cloudera.cmf.db.type=mysql
com.cloudera.cmf.db.host=ec2-54-251-190-59.ap-southeast-1.compute.amazonaws.com
com.cloudera.cmf.db.name=scm
com.cloudera.cmf.db.user=scm
com.cloudera.cmf.db.password=scm_password
com.cloudera.cmf.db.setupType=EXTERNAL

```