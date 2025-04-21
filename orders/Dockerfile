FROM python:3.9-alpine

# Copiar el archivo requirements.pip
ADD requirements.pip requirements.pip

# Instalar dependencias
RUN pip3 install --no-cache-dir -r requirements.pip

# Copiar el código fuente
ADD src src

EXPOSE 5000

CMD ["python3", "/src/run.py"]
