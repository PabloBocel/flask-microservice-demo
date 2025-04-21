FROM python:3.9-alpine

# Instalar dependencias y asegurarnos de que pip3 esté disponible
RUN apk update && apk add --no-cache python3 py3-pip

# Añadir el archivo de requerimientos y ejecutar pip
ADD requirements.pip /requirements.pip
RUN pip3 install --no-cache-dir -r /requirements.pip

# Copiar el código fuente
ADD src /src

EXPOSE 5000

CMD ["python3", "/src/run.py"]
