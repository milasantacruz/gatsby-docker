
## Development Container For GatsbyJS
hange the develop script to this:
"develop": "gatsby develop -H 0.0.0.0"

## About docker and compose

Compose works in all environments: production, staging, development, testing, as well as CI workflows. You can learn more about each case in Common Use Cases.

Using Compose is basically a three-step process:

    1) Define your app’s environment with a Dockerfile so it can be reproduced anywhere.

    2) Define the services that make up your app in docker-compose.yml so they can be run together in an isolated environment.

    3) Run docker compose up and the Docker compose command starts and runs your entire app. You can alternatively run docker-compose up using the docker-compose binary.

## Compose has commands for managing the whole lifecycle of your application:

    - Start, stop, and rebuild services
    - View the status of running services
    - Stream the log output of running services
    - Run a one-off command on a service

## Features

The features of Compose that make it effective are:

    - Multiple isolated environments on a single host
    - Preserve volume data when containers are created
    - Only recreate containers that have changed
    - Variables and moving a composition between environments

**About start the container**
**Running Development:**
Once you have all of your files setup, you can start your containers with the following command:

``docker-compose up``

Or if you need to rebuild your Docker image(the Dockerfile.dev)

``docker-compose up --build``

**Running Production:**

Once you're done working on your Gatsby website, and finished with development, you run the production version of your website via:

``docker-compose -f docker-compose.prod.yml up``

And make sure to add the build tag if you have updated your gatsby website.

``docker-compose -f docker-compose.prod.yml up --build``