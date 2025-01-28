# Utiliza una imagen oficial de Python basada en Alpine con una versión compatible
FROM python:3.9-alpine

# Establece el directorio de trabajo
WORKDIR /usr/src/app

# Copia el archivo de requerimientos
COPY requirements.txt ./

# Actualiza pip a la última versión
RUN pip install --upgrade pip

# Instala las dependencias de la aplicación
RUN pip install --no-cache-dir -r requirements.txt

# Copia el resto de los archivos de la aplicación
COPY . .

# Especifica el comando por defecto
CMD ["python", "app.py"]
