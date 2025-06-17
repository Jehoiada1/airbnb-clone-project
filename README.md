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
