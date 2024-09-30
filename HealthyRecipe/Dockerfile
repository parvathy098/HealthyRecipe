# Use an official Node.js runtime as the base image
FROM node:16

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json (if available)
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of your application files into the container
COPY . .

# Expose the port the app runs on
EXPOSE 3055

# Command to run your application
CMD ["npm", "start"]
