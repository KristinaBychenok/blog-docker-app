FROM node:22-alpine

RUN mkdir -p /home/app/frontend

WORKDIR /home/app/frontend

COPY ./package.json /home/app/frontend/

RUN npm install

COPY . /home/app/frontend/

# Build the React app
RUN npm run build

# Install a lightweight static file server to serve the build folder
RUN npm install -g serve

# Expose the port the app runs on
EXPOSE 3000

# Command to serve the React app
CMD ["serve", "-s", "build", "-l", "3000"]

# CMD ["node", "src/index.js"]