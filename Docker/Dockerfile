# Use the lightweight Node.js 20 base image
FROM node:20-alpine

# Set the working directory
WORKDIR /app

# Copy dependency files first (for caching)
COPY package*.json ./

# Install dependencies
RUN npm install --production

# Copy the entire application code
COPY . .

# Expose port for incoming requests
EXPOSE 5000

# Start the Node.js application
CMD ["node", "server.js"]