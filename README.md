# Docker Compose PHP+MYSQL on OSX

This setup is great for writing quick apps in PHP from an OSX machine. It uses Virtualbox and machine to create the actual environment and then uses compose to setup the application services


### Install docker, compose, and machine (or Docker Toolbox)

```
brew update
brew install docker docker-compose docker-machine
```


### InstallVirtualbox
[Download Virtualbox](https://www.virtualbox.org/wiki/Downloads)

### Setup docker environment

```
docker-machine create --driver virtualbox --virtualbox-memory "2048" --virtualbox-disk-size "10000" lemp
docker-machine start lemp
eval $(docker-machine env lemp)
```

### Build & Run!

```
docker-compose build
docker-compose up -d
```
you can now start writing your app!

### Stop

```
docker-compose kill
```

### MySQL

Check out `app/index.php` for getting credentials from the ENV variables.
