# Usa la imagen base de Python 3.12 en Alpine Linux
FROM python:3.12-alpine3.17

# Define el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia el archivo de dependencias
COPY requirements.txt requirements.txt

# Instala las dependencias necesarias
RUN pip install -r requirements.txt

# Copia todo el contenido del proyecto al contenedor
COPY . .

# Expone el puerto 5000 para la aplicación Flask
EXPOSE 5000

# Comando para iniciar Flask (asegura que acepte conexiones externas)
CMD ["python", "-m", "flask", "run", "--host=0.0.0.0"]
