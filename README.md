# docker-cpp-opencv3-dlib

## BUILD
```
docker build -t docker-cpp-opencv3-glut .
```
## RUN
```
docker run -ti -v $(pwd):/usr/src/app docker-cpp-opencv3-glut /bin/sh
cd /usr/src/app-build
cmake /usr/src/app/
cmake --build /usr/src/app-build --config Release
```
