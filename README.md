# Parking Lot Management System

## Overview
The **Parking Lot Management System** is a robust and scalable solution built using **Spring Boot** to handle parking operations efficiently. It manages vehicle parking, gate operations, billing, payments, and real-time status updates while covering all possible edge cases.

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

## API Endpoints
| Endpoint                  | Method | Description |
|---------------------------|--------|-------------|
| `/api/parkinglot/create`  | POST   | Create a new parking lot |
| `/api/gate/open/{id}`     | PUT    | Open a gate |
| `/api/gate/close/{id}`    | PUT    | Close a gate |
| `/api/ticket/generate`    | POST   | Generate a parking ticket |
| `/api/ticket/{id}`        | GET    | Retrieve ticket details |
| `/api/payment/make`       | POST   | Make a payment |
| `/api/payment/status/{id}`| GET    | Get payment status |
| `/api/parkinglot/status`  | GET    | Get overall parking lot status |

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
3. Build and run the application:
   ```sh
   mvn clean install
   mvn spring-boot:run
   ```

## License
This project is licensed under the MIT License.

