FROM python:3.6-slim
RUN mkdir /opt/app
COPY requirements.txt /opt/app
RUN pip3 install -r /opt/app/requirements.txt

WORKDIR /opt/app
CMD /bin/bash
