# Use official Node.js LTS image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the app
COPY . .

# Build the app (only needed for Next.js or similar frameworks)
RUN npm run build

# Expose port (adjust if needed)
EXPOSE 3000

# Start the app
CMD ["npm", "start"]
