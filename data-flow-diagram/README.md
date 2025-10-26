# Airbnb Clone — Data Flow Diagram (DFD)

The Data Flow Diagram shows how data moves between users, backend processes, and databases.

## 🧩 Key Entities
- User
- Property
- Booking
- Payment

## 💡 Data Flows
1. User submits login info → Auth Controller → Database (verify credentials)
2. Host submits new property → Property Controller → Database (store listing)
3. Guest books a property → Booking Controller → Database (create booking)
4. Guest makes payment → Payment Gateway → Payment Controller → Database (save transaction)
5. Guest leaves a review → Review Controller → Database (store review)

## 📤 Export
Diagram exported as: `data-flow.png`

**Location:**  
`data-flow-diagram/data-flow.png`
