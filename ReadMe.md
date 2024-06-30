# DevOps Task

Follow the instructions below to get your application up and running.

## Building the Docker Image

1. **Navigate to the project directory**: Open your terminal or command prompt and change the directory to where your project is located.

```sh
cd /path/to/your/project
```

2. **Build the Docker image**: Execute the following command to build the Docker image. This command reads the `Dockerfile` in your current directory and constructs the image.

```sh
docker build -t devops-task:latest .
```

- `docker build`: The command to build a Docker image.
- `-t devops-task:latest`: Tags the image with the name `devops-task` and the tag `latest`. This makes it easier to reference the image later.
- `.`: Specifies the current directory as the build context, where the `Dockerfile` is located.

## Running the Docker Container

After building the Docker image, you can run it as a container. The container is an instance of the Docker image, running as an isolated application.

1. **Run the Docker container**: Use the following command to start the container.

```sh
docker run -itd --rm -p 9000:80 devops-task:latest
```

- `docker run`: The command to run a Docker container.
- `-itd`: Runs the container in interactive mode (`-i`), attaches a terminal (`-t`), and detaches it to run in the background (`-d`).
- `--rm`: Automatically removes the container when it exits, preventing leftover stopped containers from accumulating.
- `-p 9000:80`: Maps port 9000 on your host machine to port 80 in the container. This allows you to access the application via `http://localhost:9000`.
- `devops-task:latest`: Specifies the image to run, using the name and tag created during the build step.

## Accessing the Application

Once the container is running, your application will be accessible in your web browser at:

[http://localhost:9000](http://localhost:9000)

This URL directs your browser to the application running inside the Docker container.

## Managing the Docker Container

### Viewing Running Containers

To see a list of all running containers, use the following command:

```sh
docker ps
```
