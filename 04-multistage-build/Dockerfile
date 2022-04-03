# Use node image to build production files
FROM node:16-alpine as builder
WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

# Each FROM instruction can use a different base,
# and each of them begins a new stage of the build.

FROM nginx
# Copy production files (artifact) from previous stage
# to a new container using NGINX as base image
COPY --from=builder /app/build /usr/share/nginx/html

# Read more
# https://docs.docker.com/develop/develop-images/multistage-build/