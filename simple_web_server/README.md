*alpine* is a very small, lightweight Linux distribution. 

*nginx*, by default, serves files from `/usr/share/nginx/html` inside the container. This path is pre-created by the nginx image.

Port 80 is the standard HTTP port.

No need to include a CMD in the Dockerfile because the base image *nginx:alpine* already has a CMD defined in it: `CMD ["nginx", "-g", "daemon off;"]`



