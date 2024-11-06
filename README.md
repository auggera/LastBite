LastBite (Mobile and Web Application to Reduce Food Waste)

A microservices-based educational project in active development, designed to facilitate user management, authentication, email verification, and future food offer interactions.
Project Structure: Currently includes three microservices:
· User Service: Handles user management, including registration, profile updates, and verification status tracking.
· Email Service: Manages email notifications, such as verification emails, using asynchronous processing and secure SMTP configurations.
· Token Service: Responsible for generating and validating tokens for user verification and password reset.

Planned Microservices:
· Offer Service: Allows businesses to list food offers, integrates with the User Service for managing business profiles, and supports listing offers based on user location.
· Order Service: Manages user orders and integrates with the Offer and Payment services, ensuring smooth order creation, updating, and tracking.
· Payment Service: Processes transactions securely, connecting with the Order Service to facilitate payments, applying potential discounts or loyalty points.
· Admin Service: Provides an interface for administrators to manage users, review business accounts, and handle role assignments (e.g., approving requests for the Business Owner role). This service integrates with the User Service to update user roles and manage access permissions. It will also monitor platform activity, allowing administrators to address reported issues or violations and maintain overall system integrity.
· Notification Service: This service would centralize notifications, allowing LastBite to support multi-channel notifications (email, SMS, push notifications). It would work alongside the Email Service but be more generalized to handle other types of alerts and updates.
· Analytics Service: Collects and analyzes user interactions, food offer metrics, and other data. It would provide valuable insights into user behavior, popular offers, peak activity times, and other performance metrics, which could be used to optimize the platform and enhance user experience.
· Loyalty and Rewards Service: Manages a loyalty program, allowing users to earn and redeem points for actions such as making purchases or leaving reviews. This service would integrate with the Order and Payment services to apply discounts or loyalty points to user orders.

Technologies and Tools:
· Spring Boot (for microservice development)
· Docker & Docker Compose (for containerization and orchestration)
· PostgreSQL (for relational data storage)
· H2 (used for testing)
· JUnit & Mockito (for unit and integration testing)
· GitHub Actions (for CI/CD)
· REST API (for communication between microservices)
· Jakarta Mail (for email handling in the Email Service)

Run the project
To start all microservices locally, use the command:
docker compose --env-file .env up --build

Ongoing Work:
Continuing development of additional microservices, frontend for web and mobile, and feature expansion.
