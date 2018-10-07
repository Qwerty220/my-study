# **RabbitMQ**

Платформа, реализующая систему обмена сообщениями между компонентами программной системы на основе стандарта AMQP.

### Установка

Официальный образ [https://hub.docker.com/\_/rabbitmq/](https://hub.docker.com/_/rabbitmq/)

```bash
docker run -d --hostname rabbit \
	--name rabbit \
	-p 15672:15672 \
	-v /Volumes/Data/Docker/rabbit/home:/var/lib/rabbitmq \
	-v /Volumes/Data/Docker/rabbit/conf:/etc/rabbitmq \
	-e RABBITMQ_DEFAULT_USER=admin \
	-e RABBITMQ_DEFAULT_PASS=admin \
	rabbitmq:3-management && docker exec rabbit rabbitmq-plugins enable rabbitmq_management

```

[http://localhost:15672/\#/](http://localhost:15672/#/)

![](/assets/4633.png)

