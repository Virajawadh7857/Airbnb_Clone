# 🏡 Property Booking System (Airbnb Clone)

A full-stack **Airbnb-like Property Booking Application** where users can register as guests to book properties or as hosts to list their own properties. Admin users manage and monitor all platform activity. This project showcases a real-world use case using modern backend and DevOps technologies.

---

## 🔥 Key Features

### 🧑‍💼 Admin:
- Manage all user accounts (Guests & Hosts)
- Approve or reject property listings
- Monitor all bookings and revenue
- View reports and platform statistics

### 👤 Guest (User):
- Register/Login as a guest
- Browse properties by location, price, date, etc.
- Book a property with custom date selection
- View booking history and cancel bookings

### 🏠 Host:
- Register/Login as a host
- Add/edit/delete property listings
- Manage availability and pricing
- View booking requests and confirm bookings

---

## 🧑‍💻 Tech Stack

| Layer         | Technology Used                     |
|---------------|-------------------------------------|
| Backend       | Java 17, Spring Boot, Spring MVC, REST APIs |
| ORM & DB      | Hibernate, MySQL                    |
| Frontend      | Angular (or React) *(Optional)*     |
| API Tools     | Postman, Swagger                    |
| DevOps        | Docker, Docker Compose, NGINX, AWS EC2 |
| CI/CD         | Jenkins / GitHub Actions *(Optional)* |
| Security      | Spring Security / JWT Auth          |

---

## 📁 Project Structure

project-root/
│
├── backend/
│ ├── src/main/java/
│ │ └── com/bookingapp/
│ │ ├── controller/
│ │ ├── service/
│ │ ├── model/
│ │ └── repository/
│ └── resources/
│ └── application.properties
│
├── docker/
│ ├── Dockerfile
│ ├── nginx.conf
│ └── docker-compose.yml
│
└── README.md

yaml
Copy
Edit

---

## 🚀 Getting Started

### Prerequisites
- Java 17
- MySQL
- Maven
- Docker & Docker Compose
- AWS EC2 instance (optional for deployment)

### Local Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/property-booking-app.git
   cd property-booking-app
Set up the MySQL Database

sql
Copy
Edit
CREATE DATABASE booking_app;
Configure application.properties

properties
Copy
Edit
spring.datasource.url=jdbc:mysql://localhost:3306/booking_app
spring.datasource.username=root
spring.datasource.password=yourpassword
Build and Run

bash
Copy
Edit
mvn clean install
mvn spring-boot:run
Test APIs

Import postman_collection.json into Postman

Base URL: http://localhost:8080/api/

🐳 Docker Deployment
bash
Copy
Edit
# From the root folder where docker-compose.yml is present
docker-compose up --build
Services:

app: Spring Boot application

db: MySQL

nginx: Reverse proxy

☁️ AWS Deployment Steps (Optional)
Launch an EC2 instance (Ubuntu)

Install Docker & Docker Compose

Clone the project to EC2

Run docker-compose up

Configure NGINX and domain (if needed)

Access app via http://<your-ec2-public-ip>

📌 API Highlights
Endpoint	Role	Description
POST /api/auth/register	Guest/Host	User Registration
POST /api/auth/login	All	Login & JWT Token
POST /api/properties	Host	List a new property
GET /api/properties	Guest	Browse available properties
POST /api/bookings	Guest	Book a property
GET /api/admin/users	Admin	View all users
PUT /api/admin/property/{id}	Admin	Approve/Reject property

🛡️ Security
Role-based access control (Admin, Guest, Host)

JWT-based stateless authentication

Data validation and sanitization

📈 Future Enhancements
Payment Integration (Razorpay, Stripe)

Email Notifications (SMTP/AWS SES)

Ratings & Reviews

Real-time booking calendar

Search filters by availability, price, and location

🙌 Contributing
Pull requests are welcome. For major changes, open an issue first to discuss what you would like to change or improve.

👨‍💻 Author
Viraj Awadh
Java Backend & DevOps Engineer
📧 [your.email@example.com]
🔗 LinkedIn Profile

