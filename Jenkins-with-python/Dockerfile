FROM jenkins/jenkins:lts-alpine
USER root
RUN apk update && \
 apk upgrade && \
 apk add python3 && \
 apk add python3-dev && \
 apk add py3-pip && \
 pip3 install --upgrade pip && \
 if [ ! -e /usr/bin/pip ]; then ln -s pip3 /usr/bin/pip ; fi && \
 if [[ ! -e /usr/bin/python ]]; then ln -sf /usr/bin/python3 /usr/bin/python; fi
RUN pip install alpine
RUN pip install setuptools
RUN apk add build-base
RUN apk add libffi
RUN apk add libffi-dev
RUN apk add py3-cffi
RUN apk add py3-wheel
RUN apk add libressl-dev
RUN apk add musl-dev