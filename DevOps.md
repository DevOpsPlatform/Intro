DevOps = development + operations

#### development 
	
	IDE : Eclipse, Visual sturdio, intellij, etc

	issue/project management tools -- jira, trac, service now, etc
	documention -- confluence, trac, shrepoint etc

	coding -- manage the code in the repositiory where you can easily  share with team members -- git, svn, mercural, RTC, TFS -- SCM tools
	
	build -- msbuild/nant/maven/ant/gradle etc
		compile origal code
		-compiling unit tests
		-run unit test
		-code quality check - sonar
		-secutiry check 
		packaging -- .jar, .war, .ear, .zip, .exe 1.0.0, 2.0.0
		deploy the package to pakcage/repositiory manager - nexus/JFrog artifactory
		-building image -- docker, rkt, containerd etc
		-deploy the image to pakcage/repositiory manager - nexus/JFrog artifactory

#### operations

	deployment 
		using script - powershell, shell script, python, etc
		automation - CM - ansible, cheff, puppet, octopus, etc
		containers - docker, rkt, containerd etc
		container orchestration - docker-swam, kubernetes, (openshit+k8s, helm charts + k8s, etc)

	servers for variours env to test our apps
	
	APP servers: IIS, kurl, Tomcat, weblogic, jboss, IBM WAS etc
	
	server monitor -- dynatrees, nagios, etc
	log monitor -- splunk, ELK,  etc
	
	User/Group Manager: LDAP
	
QA: Test Automation: Selenium for java, .net/C# etc

Jenkins/team-city/bamboo/CICD Runners in SCM tools(GitLab, GitHub, Bitbucket) etc
	building
	deployment
	building + deployment - CI/CD
	building + deployment(TEST --> SYST) + QA - CI/CD

	

