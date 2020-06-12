# build container from dockerfile dev
    docker build -f Dockerfile.dev .



# Run the container in interactive mode:
 docker run -it -p 3000:3000 CONTAINER_ID
 

# delete node_modules before run the container to avoid duplicated dependencies

# docker volume(refresh)
docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app <image_id>

# overriding Dockerfile Selection
docker-compose up

# Travis CI - for testing or deployment
    1. put a travis yml file at the root directory of the project
    2. then tell travis we need a copy of docker running
    3. build our image using dockerfile.dev
    4. tell travis how to run our test suite
    5. tell travis how to deploy our code to AWS