If you have an artifact in some maven repository, let's say

		<dependency>
			<groupId>mysql</groupId>
			<artifactId>mysql-connector-java</artifactId>
			<version>5.1.9</version>
		</dependency>

which is not OSGi-compatible, you can turn it into one by running
		
mvn clean install in this directory (providing a file like osgi.bnd).

You will get a jar file (like com.mysql-5.1.9), which you can copy to 
the skysail server osgi directory or commit as a new maven artifact.