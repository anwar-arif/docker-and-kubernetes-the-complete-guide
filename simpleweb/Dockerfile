# Specify a base image
FROM node:alpine

# Set SRC_DIR
ENV SRC_DIR=/usr/app

# Define current working directory
WORKDIR ${SRC_DIR}

# Copy source files
COPY . ${SRC_DIR}

# Install some dependencies
RUN npm install

# Default command
CMD ["npm", "start"]
