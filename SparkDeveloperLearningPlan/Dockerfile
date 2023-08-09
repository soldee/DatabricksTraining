FROM ubuntu:23.10

WORKDIR /home/ubuntu

RUN apt-get update
RUN apt-get install -y \
    default-jdk \
    scala \
    git \
    wget \
    curl \
    pip \
    python3.11-venv

RUN wget https://dlcdn.apache.org/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz
RUN curl https://downloads.apache.org/spark/spark-3.4.1/spark-3.4.1-bin-hadoop3.tgz.sha512 | sha512sum -c
RUN tar xf spark-3.4.1-bin-hadoop3.tgz
RUN rm spark-3.4.1-bin-hadoop3.tgz
RUN mv spark-3.4.1-bin-hadoop3 /opt/spark


RUN python3 -m venv .local

ENV SPARK_HOME=/opt/spark
ENV PATH=$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin:/home/ubuntu/.local/bin
ENV PYSPARK_PYTHON=/usr/bin/python3

RUN .local/bin/pip3 install notebook


ENV PYSPARK_DRIVER_PYTHON='jupyter'
ENV PYSPARK_DRIVER_PYTHON_OPTS='notebook --ip 0.0.0.0 --no-browser --port=8081 --allow-root'

WORKDIR /home/ubuntu/notebooks

CMD ["pyspark"]