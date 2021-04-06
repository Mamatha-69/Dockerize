# Dockerize
If we need to run this in docker use `docker-compose.yml` file and no need of `app.yml` and `db.yml`.

To run the compose file use command `docker-compose up`.

To run the same in kubenetes we dont need `docker-compose.yml` file.

Use `app.yml` and `db.yml`

In app directory build the image for app using command `docker build -t imagename .`

Give that image name in `app.yml` file under container image.

In `db.yml` give the image name that docker gives you defaulty.

Then apply the both `app.yml` and `db.yml` using commands `kubectl apply -f app.yml` and `kubectl apply -f db.yml`

Check the pods using `kubectl get pods` and check the logs using `kubectl logs podname`

Check the services using `kubectl get svc`

Then in the nodeport given we can see the output.
