FROM lapidarioz/docker-cpp-opencv3-glut

WORKDIR /usr/src/app-build

ONBUILD COPY . /usr/src/app

ONBUILD RUN cmake /usr/src/app/
ONBUILD RUN cmake --build /usr/src/app-build --config Release
