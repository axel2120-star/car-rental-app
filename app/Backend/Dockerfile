FROM node:18

WORKDIR /app

# Copy only package files first (IMPORTANT)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy rest of the code
COPY . .

EXPOSE 3000

CMD ["npm", "start"]