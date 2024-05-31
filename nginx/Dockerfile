FROM nginx:latest

COPY nginx.template.conf /nginx.template.conf

ENV DOCKER_MIRROR_REGISTRY_ADDRESS 10.50.0.2

CMD ["/bin/sh" , "-c" , "envsubst '${DOCKER_MIRROR_REGISTRY_ADDRESS}' < /nginx.template.conf > /etc/nginx/nginx.conf && exec nginx -g 'daemon off;'"]
