## What is AMQP?

AMQP stands for Advanced Message Queuing Protocol. It is an open standard application layer protocol for message-oriented middleware.

## What does `guest:guest@localhost:5672` mean?

`guest:guest@localhost:5672` is a connection string used to connect to a message broker that supports the AMQP protocol. `guest:guest` is the username and password used to authenticate with the broker. `localhost:5672` specifies the host and port where the broker is running.

## Slow Subscriber Simulation

The total number of queued messages in your RabbitMQ broker is determined by the difference between the number of messages published by the publisher(s) and the number of messages acknowledged (processed) by the consumer(s).

![Slow](https://cdn.discordapp.com/attachments/314315831465213953/1232367727168061522/image.png?ex=66293362&is=6627e1e2&hm=728ed4bdd27e6ee9036ebb206caaee4b518df1c4f4058138e27590fdfb7e1a98&)

## Running atleast three subscribers

This behavior is due to the nature of RabbitMQ's message distribution, which uses a round-robin scheduling by default. When multiple consumers (subscribers) are listening to the same queue, RabbitMQ will distribute the messages evenly among them.

![Console](https://cdn.discordapp.com/attachments/314315831465213953/1232373674233954424/image.png?ex=662938ec&is=6627e76c&hm=113eaa361dbccf8e5601d6b3f33eb6e7bc8cfddd58ed93a79f4b7d5933ba374c&)

![Chart2](https://cdn.discordapp.com/attachments/314315831465213953/1232373751576920154/image.png?ex=662938fe&is=6627e77e&hm=74e6c3ef0570a45bdcb9ea5fab19f14ff61d1f88bf50959e71c8e50d996ae396&)

