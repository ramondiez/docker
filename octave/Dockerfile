# Use latest debain wheezy image as the base
FROM debian:wheezy
MAINTAINER Ramón Díez Lejarazu (ramon.diez.lejarazu@gmail.com)

# Install dev tools to compile
RUN apt-get update && apt-get install -y octave

# House cleaning
RUN apt-get autoclean

# Set display
# ENV DISPLAY :0

#VOLUME ["/projects"]

CMD ["octave"]


#XSOCK=/tmp/.X11-unix
#xhost +SI:localuser:root
#docker run -t -i --rm -v $XSOCK:$XSOCK:ro -e DISPLAY=unix$DISPLAY fara/octave
#xhost -SI:localuser:root

#docker run -t -i --rm  --volume="$HOME/.Xauthority:/root/.Xauthority:rw" -e DISPLAY=unix$DISPLAY fara/octave

docker run -it --rm \
    --user=$(id u) \
    --env="DISPLAY" \
    --volume="/etc/group:/etc/group:ro" \
    --volume="/etc/passwd:/etc/passwd:ro" \
    --volume="/etc/shadow:/etc/shadow:ro" \
    --volume="/etc/sudoers.d:/etc/sudoers.d:ro" \
    --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" \
fara/octave
