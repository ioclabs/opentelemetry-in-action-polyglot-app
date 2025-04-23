# OpenTelemetry in Action: Understanding the Architecture of a Polyglot Application

This repository is based on the **Linux Foundation's LFS148** course, demonstrating how to implement **OpenTelemetry** in a polyglot microservices application. The original project has been extended and adapted to suit my personal use case, integrating **Spring Boot**, **Flask**, **PostgreSQL**, and **Docker** to showcase the power of observability through OpenTelemetry.

## 🛠️ Architecture Overview

The application is a ToDo list system built with a polyglot architecture using a mix of technologies, instrumented with OpenTelemetry to provide end-to-end observability.

### Core Components

1. **REST Server (Spring Boot + PostgreSQL)**
   - A Spring Boot-based RESTful service interacts with a PostgreSQL database to manage the ToDo list, performing CRUD operations.

2. **Frontend (Thymeleaf + Spring Boot)**
   - The Thymeleaf frontend is implemented in Java, rendering views dynamically and interacting with the Spring Boot backend to display the ToDo tasks.

3. **Alternative Frontend (Flask + Python)**
   - This component is an alternative frontend using Flask, demonstrating how Python-based services can interact with the same backend.

4. **Load Generator**
   - A load generator simulates high-traffic scenarios by repeatedly interacting with the frontends, providing insights into system performance under load.

5. **Database (PostgreSQL)**
   - PostgreSQL serves as the data store for all ToDo list data, accessed by the backend and frontend components.

## 🚀 Getting Started

### 1. Clone the Repository

To get started, clone this repository to your local machine:

```bash
git clone https://github.com/ioclabs/opentelemetry-in-action-polyglot-app.git
cd opentelemetry-in-action-polyglot-app
```

2. Set Up with Docker Compose
Use Docker Compose to set up the application stack, which includes the backend, frontends, OpenTelemetry Collector, Jaeger, and Prometheus:

```
docker compose up --build
Once the services are running, you can access:
```

Jaeger UI: http://localhost:16686

Prometheus UI: http://localhost:9090

Flask Frontend: http://localhost:5001

Thymeleaf Frontend: http://localhost:8090

3. Interact with the Application

Both the Flask and Thymeleaf frontends allow you to interact with the ToDo list:

Add, mark as done, and delete tasks.

Observe the "Sample" item, which is automatically created and removed by the load generator.

4. Monitoring with Jaeger and Prometheus

Jaeger: Use Jaeger for distributed tracing, allowing you to visualize service interactions and identify bottlenecks.

Prometheus: Monitor key metrics, such as JVM thread count and memory usage, to keep track of system performance.

🧑‍💻 Contributing

This repository is based on the Linux Foundation LFS148 course materials, which I have extended and customized for my personal use case. @ibraheemcisse contributed to adapting the application by adding OpenTelemetry instrumentation to achieve enhanced observability.

While the project itself is based on the LFS148 curriculum, feel free to fork this repository, create issues, or submit pull requests to improve the observability setup or expand on the project further.

⚙️ Technologies Used

Spring Boot (Java)

Flask (Python)

Thymeleaf (Java)

PostgreSQL

Docker

OpenTelemetry (Distributed Tracing, Metrics, and Logs)

Jaeger (Distributed Tracing Visualization)

Prometheus (Metrics Monitoring)

📜 License

This project is based on the Linux Foundation's LFS148 curriculum and is subject to the applicable terms. All modifications to this repository are licensed under the MIT License - see the LICENSE file for details.
