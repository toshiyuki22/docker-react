# build container from dockerfile dev
    docker build -f Dockerfile.dev .



# Run the container in interactive mode:
 docker run -it -p 3000:3000 CONTAINER_ID
 

# delete node_modules before run the container to avoid duplicated dependencies

# docker volume(refresh)
docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app <image_id>

# overriding Dockerfile Selection
docker-compose up