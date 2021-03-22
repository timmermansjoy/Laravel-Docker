# Laravel-Docker

## Requrements

All you need to use this project is to have [docker desktop](https://www.docker.com/products/docker-desktop) installed on your computer.

## Instalation

- cange the `env` file to `.env`.
- add your project folder to this folder and add change the path in the `.env` file to the project you put inside this folder.

## Use

When you have setup everything you can open this project in your IDE and open the terminal or navigate to this project. once in you can run

```zsh
docker-compose up -d --build
```

to run this docker. the first time it will download everything from the docker hub and set the containers up for you

When you want to stop the containers run

```zsh
docker-compose down
```

for running commands like artisan you have to write `docker-compose run --rm` in front of the command so the containers will execute your command.
Example

```
docker-compose run --rm artisan migrate:fresh --seed

docker-compose run --rm composer update

docker-compose run --rm npm install

docker-compose run --rm run dev
```

As you can see we dont write php in front of artisan or composer. this will be handeld for you.

## Disclaimers

This project is optimized to run as a development envoirment out of the box. not a production ready enviorment.

If you have any sugestions to improve this setup / workflow. You can let me know

## References

[Andrew Schmelyun](https://www.youtube.com/user/ASchmelyun)
