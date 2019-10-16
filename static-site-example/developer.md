We will us docker to run an image that will be automatically downloaded if you don't already have it. We will then navigate to it in a browser and hit a server that's running inside an nginx container.

$ docker run --rm prakhar1989/static-site //here the --rm will automatically remove it once it exits
$ docker run -d -P --name static-site prakhar1989/static-site //Here -d is for detached so we can close terminal window and -P publishes exposed ports randomly and we give it a name
$ docker port static-site

Visit the 80/tcp -> 0.0.0.0:32769 (in our case we were assigned 32769, you could get something different) in browser via localhost:32769
Alternatively run the following to use port 8888:
$ docker run -p 8888:80 prakhar1989/static-site

