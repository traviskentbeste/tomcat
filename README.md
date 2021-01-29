# Apache Config

```
<VirtualHost *:80>
ProxyPreserveHost On
ProxyRequests     Off
ServerName        <hostname>
ProxyPass         / http://localhost:5555/tomcat/
ProxyPassReverse  / http://localhost:5555/
</VirtualHost>
```

# Tomcat config
* this goes in the conf/server.xml.  Notice the port number needs to match above
```
<Connector
port="5555"
proxyName="vendingtestingandrepair.com"
proxyPort="80"
/>
```