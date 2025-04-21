FROM python:3.9-slim

WORKDIR /app

COPY requirements.pip requirements.pip

RUN pip install --no-cache-dir -r requirements.pip

COPY src/ src/

EXPOSE 5000

CMD ["python", "src/run.py"]
