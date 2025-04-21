# Usar una imagen de Python basada en Alpine
FROM python:3.9-alpine

# Copiar el archivo de requerimientos
ADD requirements.pip /requirements.pip

RUN python3 -m pip --version

# Instalar las dependencias desde requirements.pip
RUN pip3 install --no-cache-dir -r /requirements.pip

# Copiar el código fuente
ADD src /src

EXPOSE 5000

CMD ["python3", "/src/run.py"]
