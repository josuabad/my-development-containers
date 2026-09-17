# Jupyter Notebook Custom Environment

## Pasos para usar el Dockerfile:

1. **Guardar el archivo:** Guarda el contenido anterior en un archivo llamado `Dockerfile` (sin extensión) o renombra el archivo descargado.

2. **Construir la imagen:**

```bash
docker build -t my_jupyterlab_image:latest .

```

3. **Ejecutar el contenedor:**

```bash
docker run -d --rm -p 8888:8888 -v ${PWD}:/workspace --name my_jupyter_container my_jupyterlab_image:latest
```

4. **En caso de reintento:**

```bash
docker compose build --no-cache

```
