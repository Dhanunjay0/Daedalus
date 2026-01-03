# Use a lightweight Node.js version
FROM node:20-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package files first (to leverage Docker caching)
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the rest of your application code
COPY . .

# Expose the port your Express app runs on
EXPOSE 5000

# Command to run the app in dev mode (ensure you have "dev": "nodemon src/server.ts" in package.json)
CMD ["npm", "run", "dev"]
