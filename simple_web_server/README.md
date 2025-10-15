*alpine* is a very small, lightweight Linux distribution. 

*nginx*, by default, serves files from `/usr/share/nginx/html` inside the container. This path is pre-created by the nginx image.

Port 80 is the standard HTTP port.

No need to include a CMD in the Dockerfile because the base image *nginx:alpine* already has a CMD defined in it: `CMD ["nginx", "-g", "daemon off;"]`

Here are the commands to build the image and run the container:

Build the docker image:
```bash
docker build -t mynginxapp .
```

Run docker container:
```bash 
docker run -d -p 80:80 --name mynginxapp mynginxapp 
```


