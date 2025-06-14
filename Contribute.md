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
- Start postgres
    - docker run -r POSTGRES_PASSWORD=mypass -d -p 5432:5432 postgres
- Build the image - `docker build -t user-project`
- Start the image - `docker run -p 3000:3000 user-project`

## Docker compose installation steps
- Install docker, docker-compose
- Run `docker-compose up`