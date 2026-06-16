FROM node:22-alpine
WORKDIR /usr/src/app
COPY servicios/servicio-usuario/package*.json ./
RUN npm install
COPY servicios/servicio-usuario/ .
RUN npx prisma generate
EXPOSE 4102
CMD ["npm", "run", "dev"]
