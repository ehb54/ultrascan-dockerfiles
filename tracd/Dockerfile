FROM debian:latest

EXPOSE 80/TCP

RUN apt-get update
# RUN apt-get install -y --no-install-recommends apt-utils 
RUN apt-get install -y python3 python3-pip
RUN apt-get install -y python3-full
RUN pip install --break-system-packages https://download.edgewall.org/trac/Trac-1.6.tar.gz

