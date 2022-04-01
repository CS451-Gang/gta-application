# Overview

## Docker Compose

1. install [docker compose](https://docs.docker.com/compose/install/)
2. run `docker-compose up --build` to build and launch all 3 containers together
   - frontend: http://localhost:3000/public/login
   - backend:  http://localhost:8000/api
3. when you're done, run `docker-compose down -v --remove-orphans --rmi all ` to stop the containers and delete their resources

# Assumptions

- [X] Students only apply for positions they're qualified for. Verification is performed by faculty.
- [X] There is no overlap between faculty and students.
- [ ] etc.