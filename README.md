## What is AMQP?

AMQP stands for Advanced Message Queuing Protocol. It is an open standard application layer protocol for message-oriented middleware.

## What does `guest:guest@localhost:5672` mean?

`guest:guest@localhost:5672` is a connection string used to connect to a message broker that supports the AMQP protocol. `guest:guest` is the username and password used to authenticate with the broker. `localhost:5672` specifies the host and port where the broker is running.

## Slow Subscriber Simulation

The total number of queued messages in your RabbitMQ broker is determined by the difference between the number of messages published by the publisher(s) and the number of messages acknowledged (processed) by the consumer(s).

![Slow](https://cdn.discordapp.com/attachments/314315831465213953/1232367727168061522/image.png?ex=66293362&is=6627e1e2&hm=728ed4bdd27e6ee9036ebb206caaee4b518df1c4f4058138e27590fdfb7e1a98&)

