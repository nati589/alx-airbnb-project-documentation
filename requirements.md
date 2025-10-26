# Airbnb Clone — Backend Requirement Specifications

## 1. User Authentication
### Description
Manages registration, login, and authentication of users.

### API Endpoints
| Method | Endpoint | Description |
|--------|-----------|-------------|
| POST | /api/auth/register | Register a new user |
| POST | /api/auth/login | Authenticate user and return JWT |
| GET | /api/users/me | Fetch logged-in user details |

### Input Validation
- Email: required, must be valid
- Password: minimum 8 characters
- Name: required

### Expected Output
- 201 Created (registration successful)
- 200 OK (login successful)
- 400 Bad Request (invalid data)
- 401 Unauthorized (invalid token)

---

## 2. Property Management
### Description
Handles property CRUD operations for hosts.

### API Endpoints
| Method | Endpoint | Description |
|--------|-----------|-------------|
| POST | /api/properties | Add new property |
| GET | /api/properties | Get all properties |
| GET | /api/properties/:id | Get single property |
| PUT | /api/properties/:id | Update property |
| DELETE | /api/properties/:id | Delete property |

### Validation
- Title, description, price, location required
- Images must be valid URLs

---

## 3. Booking System
### Description
Allows guests to book available properties.

### API Endpoints
| Method | Endpoint | Description |
|--------|-----------|-------------|
| POST | /api/bookings | Create new booking |
| GET | /api/bookings | Get user bookings |
| DELETE | /api/bookings/:id | Cancel booking |

### Validation
- Dates must not overlap existing bookings
- Payment must be confirmed before finalizing booking

---

## 4. Payment Processing
### Description
Integrates Stripe for handling payments.

### API Endpoints
| Method | Endpoint | Description |
|--------|-----------|-------------|
| POST | /api/payments/checkout | Initiate payment |
| POST | /api/payments/webhook | Handle Stripe webhook |

### Security
- All endpoints secured with JWT
- Sensitive data (cards) handled by Stripe SDK

---

## 5. Performance & Security
- JWT authentication middleware
- Password hashing with bcrypt
- Input sanitization using express-validator
- API rate limiting for brute force protection
