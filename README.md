# RabbitMQ-NodeJS
## _Demo para probar las colas en RabbitMQ_

Consiste en una aplicación en NodeJS que genera colas en RabbitMQ, 
y una aplicación de NodeJS se encarga de recibir los mensajes y sacarlos de la cola.
En este ejemplo se estudian los Exchanges Direct, Fanout y Topic.

## Instalación

- Instalar RabbitMQ en Docker
```sh
docker pull rabbitmq

docker run -d -v rabbitmq-vol:/var/lib/rabbitmq --hostname jb-rabbit -p 5672:5672 -p 8081:15672 --name jb-rabbit rabbitmq:3-management
``` 

- Levantar una instancia de la aplicación publisher
```sh
node publisher/index.js
```

- Levantar una instancia de la aplicación subscriber
```sh
node subscriber/index.js
```
