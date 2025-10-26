# 🛒 Dream Shops - Shopping Cart Backend (Spring Boot & JWT)

A complete **Shopping Cart Backend Project** built with **Spring Boot**, **Spring Security**, and **JWT Authentication**.  

## 🚀 Tech Stack

- **Java 17**
- **Spring Boot 3**
- **Spring Security**
- **JWT Authentication**
- **Spring Data JPA (Hibernate)**
- **MySQL Database**
- **Maven**
- **Lombok**
- **Stripe API** (for payment integration)

---

## ⚙️ Configuration

Make sure MySQL is running locally and update credentials if needed in  
`src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/dream_shops_db
spring.datasource.username=root
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
server.port=9191
api.prefix=/api/v1
```

# 🔑 Default Data (created automatically)

## When you first run the project, the app seeds initial data:

| Role  | Email                                       | Password |
| ----- | ------------------------------------------- | -------- |
| Admin | [admin1@email.com](mailto:admin1@email.com) | 123456   |
| Admin | [admin2@email.com](mailto:admin2@email.com) | 123456   |
| User  | [sam1@email.com](mailto:sam1@email.com)     | 123456   |
| User  | [sam2@email.com](mailto:sam2@email.com)     | 123456   |
| ...   | ...                                         | ...      |

# 🔒 Authentication (JWT)

After login, a JWT token is generated.
Use this token to access protected endpoints.

Login Endpoint
POST /api/v1/auth/login

## Request Body:

{
  "email": "admin1@email.com",
  "password": "123456"
}

## Response Example:

{
  "token": "<your-jwt-token>",
  "email": "admin1@email.com",
  "role": "ROLE_ADMIN"
}

## Add this token to your requests:

Authorization: Bearer <token>

# 🧩 Main Features

🔐 User Registration & Login (JWT Authentication)

👥 Role-Based Access Control (Admin / User)

🛍️ Product & Category CRUD Operations

🛒 Shopping Cart Management

Add / Remove / Update items

📦 Order Creation and Checkout

💳 Stripe Payment Integration

🗄️ MySQL Database with Hibernate ORM

🧰 DTOs and Validation

🧪 API tested using Postman

# 📬 API Examples (Base URL: /api/v1):

| Method   | Endpoint                | Description                     |
| -------- | ----------------------- | ------------------------------- |
| `POST`   | `/auth/login`           | Login user and return JWT token |
| `GET`    | `/products`             | Get all products                |
| `POST`   | `/products`             | Add new product (Admin only)    |
| `GET`    | `/categories`           | Get all categories              |
| `POST`   | `/cart/add`             | Add item to user’s cart         |
| `DELETE` | `/cart/remove/{itemId}` | Remove item from cart           |
| `POST`   | `/orders/place`         | Place a new order               |






