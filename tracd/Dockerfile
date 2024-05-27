FROM debian:latest

EXPOSE 8000/TCP
EXPOSE 61999/TCP
EXPOSE 54000/TCP

RUN apt-get update
# RUN apt-get install -y --no-install-recommends apt-utils 
RUN apt-get install -y python3 python3-pip
RUN apt-get install -y python3-full
RUN pip install --break-system-packages https://download.edgewall.org/trac/Trac-1.6.tar.gz
RUN apt-get install -y emacs-nox
RUN ln -s /wikis /opt/wikis

RUN apt-get install -y git
RUN git clone https://github.com/ehb54/convenience && cd convenience && ./installcont.sh
RUN rm -fr convenience
RUN apt-get install -y procps
RUN apt-get install -y telnet

CMD /opt/wikis/starttrac_all && sleep infinity


