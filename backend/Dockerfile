FROM alpine

RUN apk add --no-cache python3 py3-pip && \
    ln -sf python3 /usr/bin/python && \
    ln -sf pip3 /usr/bin/pip

ADD requirements.pip requirements.pip
RUN pip3 install -r requirements.pip

ADD src src

EXPOSE 5000

CMD ["python3", "/src/run.py"]
