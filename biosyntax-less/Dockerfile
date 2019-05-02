FROM debian:unstable

RUN apt-get update
RUN apt-get install -y biosyntax-less
RUN cat /usr/share/doc/biosyntax-less/rc_append.txt >> ~/.bashrc

#ENTRYPOINT ["/bin/bash", "-i"]
