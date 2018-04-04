FROM ubuntu:xenial

RUN apt-get update

RUN apt-get install -y apt-transport-https curl

RUN curl https://winswitch.org/gpg.asc | apt-key add -

RUN echo "deb http://winswitch.org/ xenial main" > /etc/apt/sources.list.d/winswitch.list; \
	apt-get install -y software-properties-common; \
	add-apt-repository universe; \
	apt-get update; \

	apt-get install -y xpra xterm; 





EXPOSE 18888

CMD [ "xpra start --bind-tcp=0.0.0.0:10000 --html=on --start-child=xterm"]
