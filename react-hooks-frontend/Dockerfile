
# Use the official Node.js image as a base
FROM node:14

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose port 3000 for the application
# EXPOSE 3000

# Set the environment variable to change the port
ENV PORT=80

# Expose port 80 for the application
EXPOSE 80



# Command to run the application
CMD ["npm", "start"]
