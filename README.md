Repo of Dockerfiles for Intercom Docker SDK images

You can use these Dockerfiles to build your own image or just use the ones publicly available on [Docker Hub](https://hub.docker.com/r/intercom/sdk-images/).

Feel free to suggest changes/improvements to the Dockerfiles via a branch if you have thoughts on ways to improve them.

You can either run these images using your local code and mount that into the container environment.
Alternatively, you can simply do everything in the container and not use any local code.
If you mount your local code into the container then you can use your own IDE and push to git more easily.

1/ Mount local code on dir in container
Choose the container you want (e.g. node, ruby, php or go) and then run the following command <br>
```
docker run -it --rm  -v <Absolute local dir>:<dir in container>  --env AT=”Access Token=” intercom/sdk-images:<TAG>
e.g.
docker run -it --rm  -v /home/intercom-ruby:/intercom/mount_dir --env AT=”Access Token=” intercom/sdk-images:ruby-sdk
```

Note that the directory /intercom/mount_dir was specifically added to be a mount point in the container for you local code. You can mount on and directory in the container but this will overwrite anything in that dir. So its probably better to use the mount_dir
