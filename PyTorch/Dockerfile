# Base Image: Python 3.12 Slim
FROM python:3.12-slim

ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Actualizar sistema
RUN apt-get update

WORKDIR /workspace

# Instalar librerías
RUN pip install --upgrade pip
RUN pip install --no-cache-dir jupyterlab torch numpy pandas

EXPOSE 8888

CMD ["jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root", "--NotebookApp.token=''"]
