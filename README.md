# EazyBank Microservices

EazyBank Microservices is a scalable and modular banking application built on a microservices architecture. It comprises several independent services including Accounts, Loans, Cards, a Gateway Server acting as an edge server, a Config Server for configuration management, and a Message Microservice for event streaming using Kafka.

## Features

- **Modular Design**: Each microservice focuses on a specific domain (Accounts, Loans, Cards) for better maintainability and scalability.
- **Gateway Server**: Acts as a single entry point for client requests, providing edge server capabilities such as routing, authentication, and load balancing.
- **Config Server**: Centralized configuration management for all microservices, allowing for easy configuration changes without redeploying services.
- **Message Microservice**: Implements event streaming using Kafka, enabling asynchronous communication and real-time data processing.

## Prerequisites

Before getting started, ensure you have the following installed:

- Java Development Kit (JDK) 8 or higher
- Apache Maven
- Docker
- Kafka

## Setup

1. **Clone the Repository**: 

```bash
git clone https://github.com/Nikhildevnikhil/EazyBank-Microservices.git
```

2. **Build Microservices**: 

   Navigate to each microservice directory (Accounts, Loans, Cards, Gateway, ConfigServer, Message) and build using Maven:

```bash
cd <microservice_directory>
mvn clean install
```

3. **Start Kafka**: 

   Ensure Kafka is running, as the Message Microservice relies on Kafka for event streaming.

4. **Start Microservices**: 

   Start each microservice using Docker:

```bash
docker-compose up
```

5. **Accessing Services**:

   - Gateway Server: `http://localhost:8071`
   - Other microservices endpoints can be accessed through the Gateway Server.

## Configuration

- Modify `application.properties` files in each microservice for specific configurations.
- For centralized configuration changes, update configurations in the Config Server.

## Usage

- Access the API endpoints through the Gateway Server.
- Utilize the provided endpoints for managing accounts, loans, and cards.

## Contributing

Contributions are welcome! Please fork the repository and submit pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

Special thanks to Nikhildevnikhil for creating and sharing the EazyBank Microservices repository.
