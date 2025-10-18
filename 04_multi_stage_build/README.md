Multi-stage builds separate builds and runtime envs, reducing docker image sizes.

We write a Dockerfile with two stages, the first stage builds the app, and the second stage runs the app with a lighter base image.

The application is a simple Node.js code named server.js. Node.js allows developers write JavaScript code on the server to generate dynamic web page content before sending the content to the user's web browser.

To run a Node.js project, package.json files are necessary. These files contain metadata and dependancy infromation that Node needs to install and run the app correctly.

If while building an image a warning occurs, you can see the messsage again by doing:

```bash
docker build -t node-multi-stage . --progress=plain
```

Because multi-stage build was used, the size of the created image is smaller compared to if the image was a single build. Dockerfile.single creates an image of size 1.3GB on my system, and Dockerfile.multi creats an image of size 272MB.


