# Overview

## Docker Compose

1. install [docker compose](https://docs.docker.com/compose/install/)
2. check out the `dev` branch for the `database` directory
3. in the parent directory, run `docker-compose up --build` to build and launch the database service.
4. in another terminal, run `cd frontend` and `git checkout` the appropriate branch if necessary. To start the frontend, run `npm run dev`.
5. when you're done, run `docker-compose down -v --remove-orphans --rmi all ` to stop the containers and delete their resources.


## Test Logins

Every student in the database hase a registered login of `pass` for the time being, this one was selected at random.

|          email           | password |
| :----------------------: | :------: |
|      admin@umkc.edu      |  admin   |
| nima.currie@umsystem.edu |   pass   |

# Assumptions

- [X] Students only apply for positions they're qualified for. Verification is performed by faculty.
- [X] There is no overlap between faculty and students.
- [X] The university will manage deployment details based on what makes sense for their existing technological architecture.
