# airbnb-clone-project
## Team Roles
| Name              | Role                     | Responsibilities                          |
|-------------------|--------------------------|--------------------------------------------|
| Yodahe Eshetu     | Backend Developmer       |     |

## Technology Stack

| Technology   | Purpose                                                                 |
|--------------|-------------------------------------------------------------------------|
| Django       | Backend framework for building APIs                                     |
| PostgreSQL   | Database for storing structured data                                     |
| React.js     | Frontend UI development                                                  |

## Database Design
   Key Entities & Fields
1. Users
id: Unique identifier

name: Full name of the user

email: User’s email (used for login)

password: Hashed password

role: Can be host or guest

2. Properties
id: Unique property ID

title: Property name/title

description: Details about the place

location: Address or city

price_per_night: Cost per night

3. Bookings
id: Booking ID

user_id: Foreign key referencing Users

property_id: Foreign key referencing Properties

check_in_date: Start date

check_out_date: End date

4. Reviews
id: Review ID

user_id: Foreign key referencing Users

property_id: Foreign key referencing Properties

rating: Score (1–5)

comment: User feedback

5. Payments
id: Payment ID

booking_id: Foreign key referencing Bookings

amount: Total price paid

status: Payment status (e.g., Paid, Pending)

payment_method: e.g., card, PayPal

🔗 Entity Relationships
A user can create multiple properties (if they’re a host)

A user can make multiple bookings

A property can have many bookings

A booking belongs to one user and one property

A property can have many reviews

A review is written by one user about one property

Each booking has one payment record


## Feature Breakdown

   User Authentication
Sign up with email and password

Login/logout functionality

User roles: Host and Guest

Password encryption and secure session/token handling

🏠 Property Listings
Hosts can add new listings with:

Title, description, price, images, location

Edit or delete their listings

View all properties on the home page

🔍 Search & Filter
Search by location

Filter by date, guest count, price range

Sort listings by price or rating

📅 Bookings
Guests can select check-in/check-out dates

Book a property if it's available

Booking summary and confirmation

💬 Reviews & Ratings
Guests can leave reviews after their stay

Ratings (1–5 stars) and written comments

Average rating displayed on property pages

💳 Payments
Display total booking cost

Integrate dummy or real payment methods (e.g., Stripe, PayPal)

Payment status tracking (Paid, Pending, Failed)

🌐 Responsive Frontend
Mobile-first design

Fully responsive layout (phones, tablets, desktops)

Smooth animations and transitions

🧾 Admin Features
View all users, properties, and bookings

Moderate or remove inappropriate content

Admin dashboard with stats


  ## API Security
Key Security Measures
Authentication
Users must securely log in using tokens (e.g., JWT) to verify their identity before accessing protected endpoints. This prevents unauthorized access.

Authorization
Role-based access control ensures that users can only perform actions allowed for their role (e.g., hosts can manage their listings, guests can book properties). This limits what users can do and protects sensitive data.

Rate Limiting
Limits the number of requests a client can make within a certain timeframe to prevent abuse and denial-of-service (DoS) attacks, ensuring API stability.

Data Encryption
Sensitive data (passwords, payment info) is encrypted both in transit (using HTTPS) and at rest to protect against interception and breaches.

Input Validation & Sanitization
All user inputs are validated and sanitized to prevent injection attacks like SQL injection or cross-site scripting (XSS).

Why Security Matters
Protecting User Data
Personal info such as emails, passwords, and payment details must be safeguarded to maintain user trust and comply with data privacy regulations.

Securing Payments
Payment information requires strict security to prevent fraud and financial theft, protecting both users and the platform.

Maintaining System Integrity
Preventing unauthorized access and abuse helps keep the platform reliable, available, and trustworthy.

Compliance & Reputation
Strong security practices help comply with legal standards and avoid costly breaches that damage the project’s reputation.

   ## CI/CD Pipeline

   What is CI/CD?
Continuous Integration and Continuous Deployment (CI/CD) pipelines automate the process of building, testing, and deploying code changes. This ensures that new features and fixes are delivered quickly and reliably without manual intervention.

Why CI/CD is Important for This Project
Faster Development: Automates repetitive tasks, allowing the team to focus on building features.

Early Bug Detection: Automated tests run on every code change, catching issues before deployment.

Consistent Deployments: Reduces human error by automating deployment steps.

Improved Collaboration: Helps multiple developers work together smoothly by integrating changes frequently.

Tools That Can Be Used
GitHub Actions: Integrated with GitHub, it automates workflows such as testing and deployment on code push or pull requests.

Docker: Containerizes the application, making it easy to deploy consistently across different environments.

Jenkins / CircleCI / Travis CI: Popular CI/CD platforms that support complex pipelines and integrations.

Heroku / AWS / Azure: Cloud platforms where the application can be deployed automatically after successful builds and tests.


  
