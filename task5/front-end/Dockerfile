# task2/front-end/Dockerfile
FROM nginx:latest

# Copy site files into the image
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Replace the default server config
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Document the port (Nginx will still run without this, but helpful)
EXPOSE 9000
