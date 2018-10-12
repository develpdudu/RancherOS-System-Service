# RancherOS System Service

The following is a simple Docker container to set up Linux-dash, which is a minimal low-overhead web dashboard for monitoring Linux servers. The Dockerfile will be like this:

Using the hwestphal/nodebox image, which uses a Busybox image and installs node.js and npm. We downloaded the source code of Linux-dash, and then ran the server. Linux-dash will run on port 80 by default.

To run this container in System Docker use the following command:

$ sudo system-docker run -d --net=host --name busydash husseingalal/busydash
In the command, we used --net=host to tell System Docker not to containerize the container’s networking, and use the host’s networking instead. After running the container, you can see the monitoring server by accessing http://<IP_OF_MACHINE>.