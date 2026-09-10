# Base Image: Python 3.14 Slim
FROM python:3.14-slim

ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Actualizar sistema
RUN apt-get update

WORKDIR /workspace

# Instalar JupyterLab, PySpark y librerías
RUN pip install --no-cache-dir jupyterlab scikit-learn numpy pandas matplotlib seaborn

EXPOSE 8888

CMD ["jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root", "--NotebookApp.token=''"]