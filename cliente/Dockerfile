# Usar la versión exacta de Node del proyecto
FROM node:22.22.2-alpine

# Establecer directorio de trabajo DENTRO de la carpeta cliente
WORKDIR /usr/src/app/cliente

# Copiar package.json y package-lock.json (si existe)
COPY cliente/package*.json ./

# Instalar dependencias
RUN npm install

# Copiar el resto del código del cliente
COPY cliente/ ./

# Construir la app para producción
RUN npm run build

# Exponer puerto de Next.js
EXPOSE 3000

# Comando para desarrollo o producción
CMD ["npm", "run", "dev"]