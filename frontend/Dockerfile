# Use Node.js 18
FROM node:18

# Set working directory
WORKDIR /app

# Copy package files
COPY package*.json ./

# Copy prisma schema first (needed for postinstall script)
COPY prisma ./prisma

# Install dependencies
RUN npm install

# Copy rest of source code
COPY . .

# Build app
RUN npm run build

# Expose port
EXPOSE 3000

# Start app
CMD ["npm", "start"]
