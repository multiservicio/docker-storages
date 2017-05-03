# Storage(s) [MySQL] Docker dev setup

Simple developer environment based on Docker that contains some storages (like MySQL)

It will expose (if you are using vagrant) in the normal ports. (Check ````config/docker-compose.yml```` to see which ports exactly)


## MySQL

https://hub.docker.com/_/mysql/

## How to run it

If you want to use Vagrant. Just 

````
vagrant up
````

*Note:* Some plugins are required:

```
vagrant plugin install vagrant-hostsupdater
```

We will use docker for all the services and with this plugin we can get it install quite easily.

```
vagrant plugin install vagrant-docker-compose
```


If you want to run natively Docker.

````
docker-compose -f ./config/docker-compose.yml build
docker-compose -f ./config/docker-compose.yml up -d --force-recreate
````