I need to figure out how I can get the exact tag number for an image on the hub instead of using the latest tag.

I intially used the following in my Dockerfile:
```
FROM tensorflow/tensorflow:latest
```

I got the warning that my system expectes an arm64 installation but is getting an amd64 instead. This is because I'm running the code on my Mac system. To fix this, I builr the image based on python and then ran `pip install tensorflow` in the Dockerfile.