*  jvisualvm远程监控（jstatd 及jmx）
```
jstatd -p 40123 -J-Djava.security.policy=jstatd.all.policy -J-Djava.rmi.server.hostname=10.16.11.23


java -Dcom.sun.management.jmxremote.port=40124 -Dcom.sun.management.jmxremote.ssl=false -Dcom.sun.management.jmxremote.authenticate=false -Djava.rmi.server.hostname=10.16.5.34 -jar foo.jar
java -Dcom.sun.management.jmxremote.port=40124 -Dcom.sun.management.jmxremote.ssl=false -Dcom.sun.management.jmxremote.authenticate=false -jar foo.jar

grant codebase "file:${java.home}/../lib/tools.jar" {
   permission java.security.AllPermission;
};

```
* 远程debug
```
-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=5005
```