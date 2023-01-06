# Labs

## Using: 
## Ubuntu 22.04 Jenkins server:
	A Jenkinsfile is a text file that contains the definition of a Jenkins Pipeline and is checked into source control. 
	It is typically located in the root directory of the repository.
	To create a Jenkinsfile,needs follow these steps:
	Open text editor and create a new file named "Jenkinsfile".
## Ubuntu 22.04 GitLab server:
	GitLab is a web-based Git repository manager that provides source code management (SCM), continuous integration, and more.
## Ubuntu 20.04 build server:
	To create a new node in Jenkins, needs follow these steps:
	Go to Jenkins -> Manage Jenkins -> Manage Nodes.
	Click on the "New Node" button.
	Enter a name for the node and select the "Permanent Agent" option.
	Click the "OK" button to create the node.
	For configure the node by specifying the number of executors, 
	the remote root directory, and any labels that you want to assign to the node. 
	Can also select the "Launch method" for the node, which determines how Jenkins will start the agent on the node.
   
## Jenkins configure connection to Gitlab server: 
	Jenkins used jenkins file that placed on GiTlab server
	Set up a Jenkins service in GitLab. 
	This will allow GitLab to trigger builds in Jenkins when code is pushed or a merge request is created.
	Configure the GitLab service in Jenkins. 
	Go to Jenkins -> Manage Jenkins -> Configure System and scroll down to the "GitLab" section. 
	Here can add the URL of your GitLab instance, 
	as well as the credentials for the user that Jenkins will use to authenticate with GitLab.
	Set up a Jenkins job that is triggered by a GitLab hook. 
	In Jenkins job, go to the "Build Triggers" section and check the "GitLab hook trigger for GitLab". 
	This will cause the job to be triggered whenever a merge request is created in GitLab.
	In the Jenkins job, can then set up a build step to run docker-compose.

## CI/CD using:
     Jenkins file run full pipeline operation
	/scripts/main.py:  running a Python script in a Docker containe
	/scripts/Dockerfile: the instructions for building a Docker image
	/scripts/docker-compose.yml: 
	For run and build docker file
	Docker Compose is a tool for defining and running multi-container Docker applications. 
	It allows to define the services that make up application in a single file, 
	and then use a single command to start, stop and manage all of the services.
## docker archived to storage folder 
	/scripts/scripts_labs_1_0_0_1.tar
## for run the created docker from my file need run the command:
	cd /scripts
	docker load --input scripts_labs_1_0_0_1.tar
 
## Needs doccer-engine installed:
	Docker Engine is the core component of Docker, 
	a containerization platform that allows to package, 
	deploy, and run applications in containers
## Getting started
	cd /labs/scripts
	docker-compose up --build: is a command that can use to build and start a Docker. 
	docker-compose up: is a command that can use to start a Docker Compose application.