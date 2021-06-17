FROM nginx:stable-alpine

# Alternatively I can specify workdir before I copy the html
# But I've done that in practice #01
# WORKDIR /usr/share/nginx/html

# Copy html file
COPY index.html /usr/share/nginx/html

# Doesn't need to specify CMD because will use underlying ENTRYPOINT provided by base image