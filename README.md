# Welcome to Freelo

🎉 Thank you for checking out our repository! This README will guide you through the setup and usage of our containerized application.

### Clone this Repo
To get started, clone this repository to your local machine using the following command:

```bash
git clone --recurse-submodules https://github.com/BBD-Freelo/Freelo.git
```

### Running the Containerized App 🐳
Once you've cloned the repository, you can run the containerized app using Docker Compose:

```bash
docker-compose up -d
```

### Frontend
To access the frontend of our application, simply go to [frontend](http://localhost:8080) in your web browser.

### Backend 
To access the backend of our application, navigate to [backend](http://localhost:3000).

### Database Management
If you want to see what's happening inside the database:

1. Run `docker ps` to list all running containers.
2. Get the ID or name of the PostgreSQL container (e.g., `freelo-postgres-1`).
3. Run `docker inspect freelo-postgres-1` or `docker inspect <container_id>` to inspect the container details.
4. Search for the `IPAddress` field in the JSON object. It will be under the `freelo_postgres-network`.
5. Go to [pgadmin](http://localhost:5050) for the pgAdmin container.
6. Log in with the following credentials:
    - Email: user-name@domain-name.com
    - Password: strong-password
7. Add a new server with the previously found IP address. Use the following credentials:
    - Username: postgres
    - Password: some_pass
### Deleting Containers
When you're done using the application and want to clean up, you can delete the containers using the following command:

```bash
docker-compose down -v
```
