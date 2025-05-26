FROM node:18

WORKDIR /app

# Install dependencies first (better caching)
COPY package*.json ./
RUN npm install --production

# Copy the rest of the application
COPY . .

# Create uploads directory
RUN mkdir -p uploads

# Set environment variables with defaults
ENV PORT=3000
ENV NODE_ENV=production

EXPOSE 3000

CMD ["node", "server.js"]
