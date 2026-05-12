
## Questions

a. What is amqp?
= amqp stands for Advanced Message Queuing Protocol. It is an open standard application layer protocol for message-oriented middleware. The AMQP protocol defines how messages are formatted, transmitted, and processed between different systems. It provides a way for applications to communicate with each other by sending messages through a message broker, which can route and manage the messages based on various criteria. AMQP is designed to be flexible and scalable, making it suitable for a wide range of applications, including distributed systems, microservices, and cloud-based architectures.

b. What does it mean? guest:guest@localhost:5672, what is the first guest, and what
is the second guest, and what is localhost:5672 is for?
= In the context of AMQP, "guest:guest@localhost:5672" is a connection string that specifies the credentials and address for connecting to an AMQP broker (such as RabbitMQ). The first "guest" is the username, the second "guest" is the password, "localhost" is the hostname of the broker, and "5672" is the port number on which the broker is listening. This connection string is commonly used for local development and testing, as it allows you to connect to a broker running on your local machine with default credentials. In a production environment, you would typically use different credentials and specify the appropriate hostname and port for your AMQP broker.


## Simulating Slow Subscriber


![monitoring_1](assets/monitoring_1.png)

In my machine, the total number of queue peaked at 6, which means that at one point in time, there were 6 messages in the queue waiting to be consumed by the subscriber. This happened because I simulated a slow subscriber by adding a delay of 1 second in the message handling process. As a result, when I ran the publisher program multiple times in quick succession, it sent multiple messages to the rabbitMQ server before the subscriber had a chance to consume them, leading to an accumulation of messages in the queue. The total number of queue reflects the number of messages that are waiting to be processed by the subscriber, and in this case, it peaked at 6 due to the combination of rapid message publishing and the intentional delay in message processing.