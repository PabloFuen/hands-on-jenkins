# Utiliza una imagen base oficial de Alpine Linux
FROM alpine:3.7

# Actualiza los paquetes existentes e instala Python3 y pip3
RUN apk update && \
    apk add --no-cache python3 py3-pip

# Crea el directorio de la aplicación
WORKDIR /usr/src/app

# Copia el archivo de requerimientos
COPY requirements.txt ./

# Actualiza pip a la última versión
RUN pip3 install --upgrade pip

# Instala las dependencias de la aplicación
RUN pip3 install --no-cache-dir -r requirements.txt

# Copia el resto de los archivos de la aplicación
COPY . .

# Especifica el comando por defecto
CMD ["python3", "app.py"]
