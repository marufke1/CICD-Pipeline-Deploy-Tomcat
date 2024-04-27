**PROJECT NAME: End to End CICD pipeline with jenkins, git, maven, sonarqube, nexus and war file deploying into a tomcat server.**

**PROJECT DESCRIPTION:**

This CI/CD project automates the deployment process for a Java application hosted on a GitHub repository. Leveraging Jenkins as the CI/CD tool, the pipe-line begins by fetching the source code from the GitHub repository. 

Jenkins then seamlessly integrates with Maven, the build tool, to compile the source code and generate a deployable WAR (Web Application Archive) file.

The pipeline incorporates SonarQube, a code analysis tool, to conduct com-prehensive checks on the codebase. SonarQube scans for potential bugs, vul-nerabilities, and code quality issues, producing detailed reports in XML format. These reports are crucial for maintaining code integrity and enhancing overall software quality.
Upon successful code analysis, Jenkins integrates with Nexus Artifact Reposito-ry to securely store the generated WAR file. Nexus serves as a centralized re-pository for managing dependencies and artifacts, ensuring reliable version control and efficient artifact management.

Finally, Jenkins utilizes an SSH agent to deploy the WAR file to an Apache Tomcat server. Tomcat, a widely-used servlet container, hosts the deployed application, enabling seamless deployment and continuous delivery of up-dates.

This end-to-end CI/CD pipeline streamlines the software delivery process, en-suring consistent quality, security, and reliability of the Java application.


**Server setups:**

I am using AWS cloud environment to create EC2 instances as a server for the project.  I am launching 4 instances on ubuntu Linux distribution with the instance type which is T2 MEDIUM.

Instance 1 -- installing JAVA-11, JENKINS and APACHE MAVEN.

Instance 2 – installing JAVA-11, SONARQUBE-8 for code analysis.

Instance 3 – installing JAVA-8, NEXUS ARTIFACTORY to upload the war file.

Instance 4 – installingJAVA-11, APACHE TOMCAT SERVER to deploy the war file.

Requirement to access those servers make sure need to allow the inbound rule for the instance by using default port number which are :8080 :8081: 9000: 8080 for the TOMCAT server.



