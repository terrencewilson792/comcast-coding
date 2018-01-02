# comcast-coding

Ad Server that responds to GET and POST requests

Built and tested with JDK 1.8, Ubuntu 12.04, Maven 3 and curl 7.57

This progam is a simple ad server which responds to GET and POST requests using the HTTP protocol. It can be built an run from command line on a Windows or linux-based OS with a few simple simple commands:

user@host-machine:~/ unzip ad-server.zip

user@host-machine:~/ cd ad-server

user@host-machine:~/ad-server mvn install

user@host-machine:~/ad-server /path/to/jdk/bin/java -jar target/ad-server-1.0.jar

If the port is not given, it is defaulted to 80.

The directory where it is installed is the server's document root. The server responds to GET and POST requests from curl, browsers and simple http clients like telnet or the Mozilla Firefox Poster tool.

	Send requests from curl like this: 
	1) Get all ads -> curl -XGET -H 'Content-Type:application/json' http://<server>:80/ad/
	2) Get ads by partner_id -> curl -XGET -H 'Content-Type:application/json' http://<server>:80/ad/<partner_id>/
	3) Post an ad -> curl -XPOST -H 'Content-Type:application/json' --data-binary @test.json http://<server>:80/ad/
