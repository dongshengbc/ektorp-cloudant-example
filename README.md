ektorp-cloudant-example
=======================

Very simple sample app build with ektorp running against cloudant.com. The project is pretty much build upon example
project found at http://www.ektorp.org/tutorial.html.

The project should be running out of box as follwing if you have maven installed:

<pre><code>
  mvn clean install jetty:run 
</code></pre>

Right now the project uses a [cloudant database](https://wglizeddelittleatintsfou:eSgSiFYhrcErsfsFOd2YrF62@dongshengcn.cloudant.com/blogpostdatabase/_all_docs) as a readonly user so you can not really can not create any new post.

If you want to point to your own cloudant account (so you can do write also), making the following changes: in file _src/main/resources/couchdb.properties_, replace the username and password with correct values.

<pre><code>
  host=[username].cloudant.com
  username=[username]
  password=[password]
  port=443
  maxConnections=20
  connectionTimeout=1000
  socketTimeout=10000
  autoUpdateViewOnChange=true
  enableSSL=true
  relaxedSSLSettings=true
</code></pre>

 

