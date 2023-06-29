# Usar la imagen base de Alpine
FROM alpine:latest

# Instalar NGINX
RUN apk update && apk add --no-cache nginx

# Copiar el archivo index.html al directorio raíz de NGINX
COPY index.html /usr/share/nginx/html/

# Copiar la configuración de NGINX al contenedor
COPY nginx.conf /etc/nginx/nginx.conf

# Exponer el puerto 80 para acceder al servidor web
EXPOSE 80

# Comando para iniciar NGINX en primer plano
CMD ["nginx", "-g", "daemon off;"]
