FROM alpine

# Instalar Python 3 y pip
RUN apk add --no-cache python3 py3-pip

# Copiar e instalar dependencias
ADD requirements.pip requirements.pip
RUN pip3 install --no-cache-dir -r requirements.pip

# Copiar el código fuente
ADD src src

# Exponer el puerto
EXPOSE 5000

# Comando para ejecutar la app
CMD ["python3", "/src/run.py"]
