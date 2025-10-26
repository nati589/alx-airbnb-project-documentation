# Airbnb Clone Backend — Features and Functionalities

## 1. User Authentication and Management
- User registration (signup)
- User login with JWT authentication
- Password hashing using bcrypt
- Forgot/Reset password functionality
- Update user profile
- Role management (Admin, Host, Guest)

## 2. Property Management
- Add new property (by Host)
- Update or delete property listings
- Upload property images
- Set property availability (dates)
- View all available listings
- Filter by location, price, type, or amenities

## 3. Booking System
- Search for available properties
- Make a booking reservation
- Cancel a booking
- View booking history
- Notify host on booking

## 4. Payments
- Integrate with Stripe API for secure payments
- View payment history
- Refunds and cancellations handling
- Store transaction records

## 5. Reviews and Ratings
- Guests can rate and review properties
- Hosts can respond to reviews
- Display average rating per property

## 6. Admin Features
- Manage all users and properties
- Remove inappropriate content or listings
- Monitor platform statistics

## 7. Notifications
- Email confirmation on signup
- Booking confirmation email
- Payment confirmation

## 8. Security
- JWT token validation for all protected routes
- Input sanitization
- Rate limiting for APIs

---

### 📊 Tools
- Node.js + Express.js
- PostgreSQL or MongoDB
- Stripe for Payments
- bcrypt, jsonwebtoken for authentication
- Draw.io for diagrams
