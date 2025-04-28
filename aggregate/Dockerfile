FROM python:3.9-slim

# Instalar dependencias (usando apt-get en lugar de apk)
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    python3-pip && \
    rm -rf /var/lib/apt/lists/*

# Verificar pip
RUN python3 -m pip --version

# Copiar e instalar requirements
COPY requirements.pip /requirements.pip
RUN pip3 install --no-cache-dir -r /requirements.pip

# Copiar código
COPY src /src

EXPOSE 5000
CMD ["python3", "/src/run.py"]