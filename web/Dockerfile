FROM node:18

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 5137

ENTRYPOINT [ "npm" ]

CMD ["run", "dev"]

# Command to build
# docker build --tag avatares-devops-web:v1 .

# This configuration needs a Docker network. Check if the "mynet" network is available
# docker network ls

# If it is not available, create it with the command:
# docker network create mynet

# THIS SHOULD BE THE LAST CONTAINER TO RUN
# Command to run the container
# docker run \
#   --detach \
#   --interactive \
#   --tty \
#   --env VITE_HOST=0.0.0.0 \
#   --env VITE_PORT=5137 \
#   --publish 5137:5137 \
#   --network mynet \
#   avatares-devops-web:v1

# To visualize in the explorer
# http://localhost:5173

## TODO: Investigate how to get the IP address from the API container and pass it to the WEB container as an envariable.