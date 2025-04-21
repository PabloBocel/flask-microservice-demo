FROM python:3.9-slim

# Instalar python3 y pip
RUN apk update && apk add --no-cache python3 py3-pip

# Verificar que pip3 esté disponible
RUN python3 -m pip --version

# Copiar el archivo de requerimientos
ADD requirements.pip /requirements.pip

# Instalar dependencias desde requirements.pip
RUN pip3 install --no-cache-dir -r /requirements.pip

# Copiar el código fuente
ADD src /src

EXPOSE 5000

CMD ["python3", "/src/run.py"]
