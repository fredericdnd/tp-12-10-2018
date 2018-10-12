# Base image with nginx and Node.js
FROM nginx
FROM node:carbon

# Create app directory
WORKDIR /var/docker/frontend

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)

COPY package*.json ./

# Install Node dependencies
RUN npm install

# Bundle app source
COPY . .

# Expose port 8080
EXPOSE 8080

# Run the npm start command
CMD [ "npm", "start" ]