# comcast-coding

ad-server

Ad Server that responds to GET and POST requests

This progam is a simple ad server which responds to GET and POST requests using the HTTP protocol. It is implemented in java 1.8 and can be built an run from command line on a Windows or linux-based OS with a few simple simple commands:

user@host-machine:~/ cd ad-server

user@host-machine:~/ad-server ant jar

user@host-machine:~/ad-server cd dist

user@host-machine:~/ad-server/dist /path/to/jdk/bin/java -jar ad-server.jar

The directory where it is installed is the server's document root. The server responds to GET and POST requests from curl, browsers and simple http clients like telnet or the Mozilla Firefox Poster tool.

The server can be reached with a browser by calling: "http://<host>:<port>/ad/PARTNER_ID" (to list all ads by a partner).

Post requests can be made with curl, telnet or the Firefox poster tool.

Here is a sample POST using curl:

curl -XPOST -H 'Content-Type:application/json' --data-binary @test.json http://<server>:80/ad/

The file test.json is formatted according to specifications.

Here is a sample GET request using curl:

curl -XGET -H 'Content-Type:application/json' http://<server>:80/ad/COMCAST/

If the port is not given, it is defaulted to 80.
