# Usa una imagen base de Node.js
FROM node:16-alpine

# Establece el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia los archivos package.json y package-lock.json al directorio de trabajo
COPY package*.json ./

# Instala las dependencias de la aplicación
RUN npm install

# Copia el resto de los archivos de la aplicación al directorio de trabajo
COPY . .

# Construye la aplicación NestJS
RUN npm run build

# Expone el puerto que tu aplicación utilizará
EXPOSE 3000

# Define el comando para ejecutar la aplicación
CMD ["npm", "run", "start:prod"]
