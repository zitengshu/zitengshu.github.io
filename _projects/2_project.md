---
layout: page
title: Online Programming Exercise Platform
description: A cloud native platform for pair programming
img: assets/img/ope_cover.webp
importance: 2
category: work
---

## Overview

The Online Programming Exercise Platform is designed to host scalable, interactive, and collaborative programming exercises in a cloud-native environment. Built on Kubernetes, this platform provides a multi-user experience where participants engage in tasks within JupyterLab, guided by a research-oriented chatbot. The platform supports various programming languages such as Python, MySQL, and Apache Spark, allowing users to switch roles (e.g., driver, navigator) during the exercises, mimicking a real-world pair programming scenario.

## Background

As the demand for collaborative and interactive programming environments grows, there is a need for platforms that can support real-time coding exercises while handling a large number of users concurrently. The Online Programming Exercise Platform was developed to address this need by creating a scalable, cloud-native solution that allows participants to collaborate in real-time in a JupyterLab environment.

The platform simulates real-world pair programming, where participants can rotate roles such as driver, navigator, and researcher, guided by a research-oriented chatbot. This approach mirrors real-world development workflows, making it an invaluable tool for educational purposes, coding boot camps, and collaborative learning environments.

One of the primary challenges in developing this platform was ensuring that it could scale to handle thousands of concurrent users without sacrificing performance. Additionally, real-time communication between participants needed to be seamless, reliable, and fault-tolerant. The integration of Kubernetes, Azure Communication Services, and custom Kubernetes CRDs allowed the platform to meet these challenges, resulting in a robust and scalable solution for collaborative coding.

The development of the Online Programming Exercise Platform focused heavily on optimizing resource usage, ensuring real-time collaboration, and creating a flexible environment that supports multiple programming languages and tasks. The platform continues to be an essential tool for collaborative learning and coding exercises, providing an interactive and scalable solution for developers worldwide.

## Challenges

Creating an environment where multiple users can collaborate seamlessly in real-time presented several challenges. The platform needed to support dynamic session creation and management, handle thousands of concurrent users, and provide a reliable communication infrastructure. Ensuring scalability, security, and responsiveness were key challenges throughout the development process.

## Key Contributions

- **System Architecture**: Architected the entire system on Kubernetes, incorporating stateless components for scalability and performance. Managed up to 10,000 concurrent users with efficient resource allocation and no reliance on external databases.
- **Kubernetes Operator**: Developed custom Kubernetes CRDs (`OPEUser`, `OPESession`, `OPEModule`, `OPERepository`) to manage user sessions and task assignments dynamically, ensuring that the platform can scale with demand.
- **Chatbot Integration**: Designed and implemented a fault-tolerant chatbot proxy system integrating **Azure Communication Services (ACS)**, **Bazaar**, and **Azure Event Hub** to ensure real-time communication between participants and the guiding chatbot.
- **Dynamic Session Management**: Introduced a cloud-native approach to manage static and dynamic modes for creating user sessions, handling incoming requests based on a FIFO model, and optimizing system responsiveness.
- **Scalable JupyterLab Environment**: Provided an interactive development environment within JupyterLab, supporting multiple programming languages and allowing participants to collaborate in real-time on complex coding tasks.

## Technology Stack

- **Kubernetes**: Deployed the platform as a cloud-native application, ensuring high availability and scalability through container orchestration.
- **JupyterLab**: Integrated JupyterLab as the core interactive development environment, enabling real-time collaboration on coding tasks across various programming languages.
- **gRPC**: Used gRPC for efficient communication between internal components, ensuring low-latency and reliable messaging within the platform.
- **Asyncio**: Developed the chatbot proxy using asyncio to maximize throughput, particularly in handling network-heavy operations.
- **Azure Communication Services (ACS)**: Implemented ACS for real-time chat functionality, enabling seamless interaction between participants and the research-oriented chatbot.
- **Azure EventHub**: Applied Azure EventHub for collecting and distributing messages, ensuring scalable and reliable message handling across the platform.
- **Prometheus**: Integrated Prometheus for monitoring and metrics collection, providing real-time observability of the platform’s performance.
- **Docker**: Containerized the platform for easy deployment, scalability, and management of the collaborative environment.

## Results

- **Scalability**: Successfully handled up to 10,000 concurrent users without downtime, providing a seamless and responsive experience for participants.
- **Collaboration**: Enabled real-time collaboration in a cloud-based environment, improving the effectiveness of pair programming exercises.
- **Fault Tolerance**: The platform’s robust architecture allowed for continuous operation even under high loads, ensuring reliability for users and administrators alike.

## Conclusion

The Online Programming Exercise Platform is a cutting-edge solution for collaborative coding and real-time learning. By combining Kubernetes for scalability, JupyterLab for development, and Azure Communication Services for real-time interaction, this platform delivers a highly interactive and reliable environment for coding exercises. Its cloud-native design ensures that it can scale to meet the needs of a large number of concurrent users while maintaining performance and responsiveness.
