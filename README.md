# Sample Python Docker App

## Running the app
You can run the app inside the Docker container using Docker Compose. If you want to run the container in the foreground, use the following:
```
docker-compose up --build
```
If you want to run it in the background, change it to this:
```
docker-compose up --build --detach
```

## Monitoring the container
If you've opted to run the container in the background, you can run the following command to see the status:
```
docker-compose ps
```

## Killing the container
If running in the foreground, use `Ctrl+C` to exit out of the container.

If running in the background, use the following to kill it.
```
docker-compose down
```

## Notes
The setup here is good for development use, it uses the Flask inbuilt dev server which will auto reload on changes. 

If you were to adapt this for production use, you would look to switch from using volume mounts to instead copying the source code into the image and using a server designed for production use combined with WSGI. 