# Maven Install WLS Script

This is a simple demonstration of how to install WebLogic via a Maven script. It's based
on the basic-webapp Oracle archetype. Running `mvn pre-integration-tst` will install WebLogic, 
create a domain, start the server and deploy the app. Running `mvn deploy` will do all the above
and stop the server, delete the domain and uninstall WebLogic. 

You will need to have the WebLogic 12.1.3 Install zip in your Maven repository. To do so:

- Download the zip file (from Oracle)
- Run the following:
	mvn install:install-file -Dfile=wls1213_dev.zip -DgroupId=com.oracle.weblogic -DartifactId=wls-dev -Dpackaging=zip -Dversion=12.1.3