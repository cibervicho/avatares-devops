FROM python:3.10.12-slim-bullseye
WORKDIR /avatares

COPY . .
RUN pip3 install -r requirements.txt

EXPOSE 5000

ENTRYPOINT [ "python3" ]

CMD [ "-m" , "flask", "run", "--host", "0.0.0.0", "--port", "5000"]

# Command to build
# docker build --tag avatares-devops-api:v1 .

# Command to run the container
docker run \
  --detach \
  --interactive \
  --tty \
  --env FLASK_APP=app.py \
  --env FLASK_ENV=development \
  --publish 5000:5000 \
  --network mynet \
  avatares-devops-api:v1

# To visualize in the explorer
# http://localhost:5000/api/avatar