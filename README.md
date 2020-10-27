hello-world
===========


Sample Code for a scalable and highly available webapp on gcp. The code satisfies below criteria: 

	$ Simple yet resilient application, which responds to HTTP requests.
	$ The application allows for individual node failures, without impacting availability.
	$ The application is able to scale based on load.
	$ Changes to code result in the triggering of a simple continuous integration test.
	$ A successful Build and CI test triggers an automated deployment/Upgradation with rolling ugrade.
	$ Default gcp logging and monitoring. 

## Running locally

Build and run locally:

	$ git clone https://github.com/docker/dockercloud-hello-world
	$ cd dockercloud-hello-world
	$ docker build --tag <username>/<repository>:<tag>
	$ docker run -d -p 80 <username>/<repository>:<tag>
	
## Running with Jenkins

	$ Install jenkins with docker pipeline plugin. 
	$ Edit credentialsID in jenkins file
	$ Add GOOGLE_CLOUD_KEYFILE_JSON and GOOGLE_PROJECT env variables in file /var/lib/jenkins/gcpenv files for terraform
	$ configure job and run. 
