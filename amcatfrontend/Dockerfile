FROM nginx:latest

COPY amcat.conf /etc/nginx/sites-available/amcat.conf

RUN ln -s /etc/nginx/sites-available/amcat.conf /etc/nginx/conf.d/amcat.conf

CMD ["nginx", "-g", "daemon off;"]
