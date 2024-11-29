FROM node:18

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 5173

ENTRYPOINT [ "npm" ]

CMD ["run", "dev"]

# Command to build
# docker build --tag avatares-devops-web:v1 .

# This configuration needs a Docker network. Check if the "mynet" network is available
# docker network ls

# If it is not available, create it with the command:
# docker network create mynet

# Command to run the container
# docker run \
#   --detach \
#   --interactive \
#   --tty \
#   --env VITE_HOST=0.0.0.0 \
#   --env VITE_PORT=5173 \
#   --publish 5173:5173 \
#   --network mynet \
#   avatares-devops-web:v1

# To visualize in the explorer
# http://localhost:5173