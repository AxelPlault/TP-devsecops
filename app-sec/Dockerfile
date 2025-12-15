FROM python:3.13-slim

ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1

WORKDIR /app

# Mise à jour et nettoyage (réduit la surface d'attaque)
RUN apt-get update && apt-get upgrade -y && apt-get clean && rm -rf /var/lib/apt/lists/*

# Copier le code
COPY app.py .

# Installer Flask sans cache
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir flask

EXPOSE 5000
CMD ["python", "app.py"]
