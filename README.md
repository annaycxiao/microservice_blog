# Blog Microservices Application

This is a microservices-based blog application built using a combination of React for the frontend and multiple backend services for handling different functionalities like posts, comments, query, and moderation. The app is containerized with Docker and orchestrated with Kubernetes.


## Project Overview

This project implements a microservices-based blog platform. The system is designed to demonstrate how different services can work together to create a scalable, event-driven application. Each microservice handles a distinct responsibility, allowing for flexibility, scalability, and maintainability. The application is containerized using **Docker** and orchestrated using **Kubernetes**.

### Core Features

- **Post Management:** Users can create and retrieve blog posts.
- **Comment Management:** Users can add comments to individual blog posts.
- **Moderation Service:** Automatically moderates comments, flagging any that contain inappropriate content.
- **Event Bus:** Facilitates communication between services via event-driven architecture.
- **Query Service:** Provides a unified interface for retrieving all posts and comments by aggregating data from various services.
- **React Frontend:** Offers a user-friendly interface for viewing posts and comments in real-time.

### Microservices Overview

- **Post Service**: Manages creation, updating, and retrieval of blog posts.
- **Comment Service**: Handles the creation and retrieval of comments related to posts.
- **Moderation Service**: Automatically reviews comments for inappropriate content and flags them as needed.
- **Event-Bus Service**: Responsible for event distribution between all microservices, ensuring communication and synchronization.
- **Query Service**: Aggregates data from the post and comment services to provide an optimized read interface for clients.
- **React Frontend**: The user interface where users can create posts, add comments, and view the moderated results.

Each service is built as an independent container, and the communication between them is handled through events published to the event bus.


## Tech Stack

- **Frontend**: React
- **Backend**: Node.js, Express
- **Docker**: For containerizing services
- **Kubernetes**: For container orchestration
- **Event Bus**: Custom event bus for inter-service communication