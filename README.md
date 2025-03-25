# Parking Lot Management System

## Overview
The **Parking Lot Management System** is a robust and scalable solution built using **Spring Boot** to handle parking operations efficiently. It manages vehicle parking, gate operations, billing, payments, and real-time status updates while covering all possible edge cases. Just point to be noted is that all the logics are made but the APIs are not ready.

## Features
- **Multi-Level Parking Lot Management**
- **Dynamic Spot Allocation** based on vehicle type
- **Automated Ticketing System**
- **Entry/Exit Gate Management** with different statuses
- **Real-time Billing & Payment Processing**
- **Support for Multiple Payment Modes**
- **Comprehensive Status Handling** for each parking component
- **Edge Case Handling** for overflows, billing errors, and system failures

## Tech Stack
- **Backend:** Spring Boot (Java)
- **Database:** MySQL/PostgreSQL
- **Build Tool:** Maven/Gradle
- **Authentication:** Spring Security (optional)
- **Testing:** JUnit, Mockito

## Project Structure
```
/src/main/java/com/example/parkinglot/
 ├── models/
 │   ├── BaseModel.java
 │   ├── Bill.java
 │   ├── BillStatus.java
 │   ├── Gate.java
 │   ├── GateStatus.java
 │   ├── GateType.java
 │   ├── Operator.java
 │   ├── ParkingFloor.java
 │   ├── ParkingFloorStatus.java
 │   ├── ParkingLot.java
 │   ├── ParkingLotStatus.java
 │   ├── ParkingSpot.java
 │   ├── ParkingSpotStatus.java
 │   ├── Payment.java
 │   ├── PaymentMode.java
 │   ├── PaymentStatus.java
 │   ├── Ticket.java
 │   ├── Vehicle.java
 │   ├── VehicleType.java
 ├── controllers/
 ├── services/
 ├── repositories/
 ├── exceptions/
 ├── config/
 ├── utils/
```

## Edge Case Handling
- **Overcrowding:** Prevents vehicles from entering if all spots are occupied.
- **Incorrect Payments:** Ensures validation of payment details before processing.
- **Gate Failures:** Provides alternative exits if a gate malfunctions.
- **Vehicle Type Mismatch:** Prevents vehicles from parking in incompatible spots.
- **Expired Tickets:** Automatically calculates penalties for overdue tickets.

## Setup Instructions
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/parking-lot-management.git
   cd parking-lot-management
   ```
2. Configure the database in `application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/parkinglot
   spring.datasource.username=[root]
   spring.datasource.password=[yourpassword]
   ```

## License
This project is licensed under the MIT License.

