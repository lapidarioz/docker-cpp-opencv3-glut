# docker-cpp-opencv3-glut-onbuild

## BUILD
```
docker build -t cpp-opencv3-glut-onbuild .
```

## RUN
Dockerfile
```
FROM lapidarioz/docker-cpp-opencv3-glut:onbuild
CMD [ "your-project-name" ]
```
bash
```
xhost local:root
docker run -it \
    -v $(pwd):/usr/src/app \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
		-e "DISPLAY=unix${DISPLAY}" \
    --privileged \
    your-project-image /bin/sh -c './your-project-name'
```
