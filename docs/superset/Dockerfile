# This dockerfile is for the tddv branch of superset.
# This dockerfile uses the ubuntu image as the base image.
# VERSION 0.14.1 - EDITION 1
# Author: ganshanshan
# Command format: Instrunction [arguments / command] ..

FROM ubuntu

MAINTAINER ganshanshan@gmail.com

RUN useradd -m superset

RUN apt-get update

RUN apt-get -y install \
         build-essential \
         libssl-dev \
         libffi-dev \
         python3-dev \
         python3-pip \
         libsasl2-dev \
         libldap2-dev \
	 vim

USER superset

RUN mkdir -p /home/superset/logs/superset/

RUN pip3 install pymysql

RUN pip3 --default-timeout=100 install superset_tddv

ENV PATH /home/superset/.local/bin:$PATH

ENV LC_ALL C.UTF-8

ENV LANG C.UTF-8

COPY entrypoint.sh entrypoint.sh

CMD ./entrypoint.sh

# RUN fabmanager create-admin --app superset

# RUN superset db upgrade

# RUN superset load_examples 

# RUN superset init

EXPOSE 22 8088

# CMD nohup superset runserver -p 8088 >/home/superset/logs/superset/running.log
