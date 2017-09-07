# wordpress-with-docker
Local Wordpress development with Docker.

# Setup

1) Install Docker (native app) if not already installed
    - [Docker for Windows](https://store.docker.com/editions/community/docker-ce-desktop-windows)
        - Follow Docker for Windows [configure instructions](https://docs.docker.com/docker-for-windows/#explore-the-application-and-run-examples)
    - [Docker for Mac](https://store.docker.com/editions/community/docker-ce-desktop-mac)
        - Follow Docker for Max [configure instructions](https://docs.docker.com/docker-for-mac/)
2) Change the name of this repo to project name.
3) Remove .git folder
4) Init a new Git repo
5) Edit <code>docker-compose.yml</code>
    - Change "<code>project-name-wordpress</code>" to project name
    - Change "<code>project-name-db</code>" to project name
6) Create <code>wp-app</code> folder and <code>wp-data folder</code>
    - File Structure:
        ```sh
        project-name-root
        └── wp-app
        |   └── wp-application folders
        |       └── ...
        |       └── ...
        └── wp-data
            └── project-name-db.sql files
            └── ...
        ```
7) <code>cd</code> to project root
    - Run docker commands from Project root
        - [Docker Compose documentation](https://docs.docker.com/compose/)
8) run <code>docker-compose up -d</code>
9) Open <code>localhost:8080</code> in browser
10) Follow the Worpress Install Instructions
11) When stopping the containers you can:
    1) run <code>docker container stop</code>
        - This stops the container but does not destroy it.
        - To start the container again: <code>docker container start</code>
        or
    2) run <code>docker-compose down</code>
        - This stops the container from running and destroys it.

# Database Management
1) To export the database from the database container"
    ```sh
    cd .. # to project root
    ./export.sh
    ```
    - This adds an export of the sql database to the <code>wp-data</code> folder
    

