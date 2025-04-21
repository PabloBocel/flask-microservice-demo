FROM alpine

RUN apk add --no-cache python

ADD requirements.pip requirements.pip
RUN pip install -r requirements.pip

ADD src src

EXPOSE 5000

CMD ["python", "/src/run.py"]
