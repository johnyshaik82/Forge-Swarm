--> Stop the current running docker daemon
	docker-machine stop <name>
--> Create a docker daemon
		docker-machine create --driver virtualbox <name>
		Eg: docker-machine create --driver virtualbox mydockervm
-->	Git clone this repository
--> From the docker quickstart terminal, move to the base directory of this project
		Eg: cdbookstore>
--> Execute
			cdbookstore>docker build --tag=<name>
			cdbookstore>docker run -it -p 8080:8080 <name>
			Eg: cdbookstore>docker build --tag=cdbookstore
			cdbookstore>docker run -it -p 8080:8080 cdbookstore
--> Open second docker quickstart terminal and verify 
		cdbookstore> docker ps
				This should show image cdbookstore status 'UP...'
		cdbookstore>docker-machine ls
				This should show the daemon mydockervm running and active.
		

Open browser and execute below rest end point
http://<ip>:8080/cdbookstore/rest/hello

IP in above rest call should match ip of the mydockervm appear in 'docker-machine ls' command

If everything goes ok, you should see below response in the browser

method doGet invoked: <time>

<time> is the local time of the remote wildfly server.

Happy Dockering :)
			
			