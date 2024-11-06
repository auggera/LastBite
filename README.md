# LastBite: Mobile and Web Application to Reduce Food Waste

**LastBite** is a microservices-based educational project in active development, aiming to reduce food waste by facilitating user management, authentication, email verification, and future interactions with food offers.

---

### Project Structure

The project currently consists of three core microservices:

- **User Service**: 
  - Manages user registration, profile updates, and verification status.
- **Email Service**:
  - Handles email notifications, including verification emails, using asynchronous processing and secure SMTP configurations.
- **Token Service**:
  - Responsible for generating and validating tokens for user verification and password reset.

---

### Planned Microservices

1. **Offer Service**:
   - Allows businesses to list food offers, integrating with the User Service for managing business profiles and listing offers based on user location.

2. **Order Service**:
   - Manages user orders, integrating with the Offer and Payment Services to ensure smooth order creation, updating, and tracking.

3. **Payment Service**:
   - Processes transactions securely, working with the Order Service to handle payments and apply discounts or loyalty points.

4. **Admin Service**:
   - Provides an interface for administrators to manage users, review business accounts, and assign roles (e.g., approving Business Owner requests). Integrates with the User Service for role updates and access permissions. Includes monitoring features to address reported issues or violations and maintain system integrity.

5. **Notification Service**:
   - Centralizes notifications, supporting multi-channel notifications (email, SMS, push notifications). Works alongside the Email Service but is generalized to handle a variety of alerts and updates.

6. **Analytics Service**:
   - Collects and analyzes user interactions, food offer metrics, and other data. Provides insights into user behavior, popular offers, peak activity times, and other performance metrics to optimize the platform and enhance user experience.

7. **Loyalty and Rewards Service**:
   - Manages a loyalty program, allowing users to earn and redeem points for actions like purchases or leaving reviews. Integrates with the Order and Payment Services to apply discounts or loyalty points to user orders.

---

### Technologies and Tools

- **Spring Boot**: For microservice development
- **Docker & Docker Compose**: For containerization and orchestration
- **PostgreSQL**: For relational data storage
- **H2**: For in-memory database testing
- **JUnit & Mockito**: For unit and integration testing
- **GitHub Actions**: For CI/CD automation
- **REST API**: For inter-service communication
- **Jakarta Mail**: For email handling in the Email Service

---

### Run the Project

To start all microservices locally, use the following command:

```bash
docker compose --env-file .env up --build

