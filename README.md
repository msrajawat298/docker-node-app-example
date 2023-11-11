# Dockerized Node.js App Example

This repository contains a simple example of a Node.js application dockerized with Docker Compose. The application uses the latest Node.js image from Docker Hub.

## Usage

To run the Node.js application, make sure you have Docker and Docker Compose installed on your system. Then, follow these steps:

1. Clone this repository to your local machine:
   ```git clone https://github.com/msrajawat298/docker-node-app-example.git```

2. Navigate to the project directory:
   ```cd docker-node-app-example```

3. Start the Docker containers using Docker Compose:
   ```docker-compose up```

   This command will build the Docker image and start the Node.js application in a container. The application will be accessible at `http://localhost:3000`.

4. To stop the containers, use the following command:
   ```docker-compose down```

## Configuration

The Docker Compose file (`docker-compose.yml`) defines a service named `node-app` based on the latest Node.js image. It exposes port 3000, mounts the local `./project` directory into the container at `/usr/src/app`, and sets the working directory to `/usr/src/app`.

The application is started with the following command:
   ```npm i && node app.js && tail -f /dev/null```

This command installs the project dependencies, starts the Node.js application, and keeps the container running with `tail -f /dev/null`.

Feel free to modify the `docker-compose.yml` file and the Node.js application (`app.js` and `package.json`) according to your project requirements.

Happy coding!
