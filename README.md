
## Questions

a. What is amqp?
= amqp stands for Advanced Message Queuing Protocol. It is an open standard application layer protocol for message-oriented middleware. The AMQP protocol defines how messages are formatted, transmitted, and processed between different systems. It provides a way for applications to communicate with each other by sending messages through a message broker, which can route and manage the messages based on various criteria. AMQP is designed to be flexible and scalable, making it suitable for a wide range of applications, including distributed systems, microservices, and cloud-based architectures.

b. What does it mean? guest:guest@localhost:5672, what is the first guest, and what
is the second guest, and what is localhost:5672 is for?
= In the context of AMQP, "guest:guest@localhost:5672" is a connection string that specifies the credentials and address for connecting to an AMQP broker (such as RabbitMQ). The first "guest" is the username, the second "guest" is the password, "localhost" is the hostname of the broker, and "5672" is the port number on which the broker is listening. This connection string is commonly used for local development and testing, as it allows you to connect to a broker running on your local machine with default credentials. In a production environment, you would typically use different credentials and specify the appropriate hostname and port for your AMQP broker.