## Manual Installation
- Install nodejs locally
- Clone the repo
- Install dependencies
- Start the db locally
    - docker run -e POSTGRES_PASSWORD=mypass -d -p 5432:5432 postgres
    - go to neon.tech and get a new db
- Change .env file and update db creds
-  npx prisma migrate
- npx prisma generate
- npm run build 
- npm run start

## Docker installation
- Install docker
- Create a network - `docker network create user_project`
- Start postgres
    - `docker run --network user_project --name postgres -e POSTGRES_PASSWORD=mypass -d -p 5432:5432 postgres`
- Build the image - `docker build --network=host -t user-project .`
- Start the image - `docker run -e DATABASE_URL=postgresql://postgres:mypass@postgres:5432/postgres --network user_project -p 3000:3000 user-project`

## Docker compose installation steps
- Install docker, docker-compose
- Run `docker-compose up`