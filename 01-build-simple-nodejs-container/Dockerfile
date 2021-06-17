# Use nodejs image as base image, alpine linux variant
FROM node:alpine

# Set workdir inside container
WORKDIR /usr/app

# Copy files from this working directory to container
COPY ./ ./

# Install dependencies
RUN npm install

# Set default command to run when container starts
CMD ["npm", "start"]

# Build the image using :
# docker build -t roboticpuppies/hello-node .