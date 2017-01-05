# docker-cpp-opencv3-dlib

## BUILD
```
docker build -t docker-cpp-opencv3-glut .
```
## RUN
```
xhost local:root
docker run -it \
    -v $(pwd):/usr/src/app \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
		-e "DISPLAY=unix${DISPLAY}" \
    --privileged \
    docker-cpp-opencv3-glut /bin/sh
cd /usr/src/app-build
cmake /usr/src/app/
cmake --build /usr/src/app-build --config Release
```
