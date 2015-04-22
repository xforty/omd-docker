omd-docker
==========

[Dockerfile](https://www.docker.com) for [Open Monitoring Distribution (OMD)](http://omdistro.org).

Run from Docker Hub
-------------------

A pre-built image is available on [Docker Hub](https://registry.hub.docker.com/u/glichti/omd-docker) and can be run as follows:

    docker run -t -p 80:5000 --name 'omd-docker' --hostname 'omd-docker' glichti/omd-docker

This will leave a shell open to access the container.

OMD will become available on [http://172.X.X.X/default](http://172.X.X.X/default).
The default login is `omdadmin` with password `omd`.
To find out the IP address, run `ip addr` in the container shell.

Build from Source
-----------------

The Docker image can be built as follows:

    git clone https://github.com/glichti/omd-docker
    cd omd-docker
    docker build -t="glichti/omd-docker" .
