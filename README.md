<<<<<<< HEAD
# Smart-Home-Automation

This project implements a smart home automation system using Java using linked list and priority queue, and asynchronous programming for device management and rule execution.  It allows for the creation, control, and monitoring of smart home devices, also power and battery management features along with logging.  A REST API is provided for interaction.

## Python Code
[Python code for the project](https://github.com/duckyies/Smart-Home-Automation)

## Docs
[Documentation for the code can be found here](https://duckyies.github.io/Smart-Home-Automation-Java/)

## Setup and Running

1. **Prerequisites:**
    * Ensure you have JDK installed.
    * Install Maven or Gradle.
    * Install MongoDB.


2. **Clone the repository:**

   ```bash
   git clone <repository_url>
   ```

3. **Build the project:** (using Maven)

   ```bash
   mvn clean install
   ```

4. **Run the application:**

   ```bash
   mvn spring-boot:run
   ```

## API Endpoints

(See `SmartHomeController.java` for a complete list and descriptions.)

## Features

* **Device Management:**
    * Create and add devices (with various attributes like type, group, location, power level, and battery information).
    * Turn devices on/off individually or by group, type, or location.
    * Remove devices.
    * Retrieve device information (name, type, status, power consumption, battery level).
* **Power Management:**
    * Monitors overall power consumption.
    * Implements a power reduction strategy to stay below a defined threshold.  This involves turning off lower-priority devices if the threshold is exceeded.
    * Provides real-time power consumption feedback.
* **Battery Management:**
    * Tracks battery levels for battery-powered devices.
    * Issues warnings and errors when battery levels are low.
    * Automatically turns off devices when their battery is depleted.
* **Rule Engine:**
    * Defines and executes rules for automated device control.  Rules can be added dynamically at runtime.
    * Supports various rule types:
        * `flip [deviceId/deviceName]`: Toggles the power state of a device.
        * `turn [deviceId/deviceName] on/off`: Turns a device on or off.
        * `set [deviceId/deviceName] powerLevel`: Sets the power level of a device.
        * `group [groupName] on/off`: Turns all devices in a group on or off.
        * `type [typeName] on/off`: Turns all devices of a type on or off.
        * `location [locationName] on/off`: Turns all devices in a location on or off.
* **Location and Temperature Management:**
    * Manages device locations and their temperatures.
    *  Provides temperature monitoring and alerts.
    *  Intelligent Air Conditioner control: Automatically adjusts the Air Conditioner based on the desired ideal temperature and current location temperature.
* **Logging:**
    * Logs various events to separate files (info, warning, severe, power consumption, battery).  Log levels are configurable.
    * Provides a REST endpoint to retrieve the logs.
* **REST API:**
    * Exposes a RESTful API for interacting with the smart home system (using Spring Boot).
    * Allows for remote device control and data retrieval.
* **Asynchronous Operations:**  Uses `@Async` annotations for non-blocking operations.
* **Data Structures:** Use custom and standard Java data structures for efficient device and task management (LinkedList, PriorityQueue, ConcurrentHashMap).


## Technology Stack

* Java
* Spring Boot (for REST API)
* MongoDB (for persistence)

## Future Enhancements

* **User Authentication and Authorization:**
* **Device Discovery:** 
* **More Sophisticated Rule Engine:**  A
* **Integration with other Smart Home Platforms:**
* **Improved UI:**
* **Real-time data visualization**
=======
# 🏠 Smart Home Automation System

A Java-based Smart Home Automation System designed to manage, monitor, and automate smart devices through rule-based control, intelligent power management, battery monitoring, and temperature regulation.

The project uses **Java, Spring Boot, REST APIs, and MongoDB** to provide a modular system for smart device management. It also demonstrates the practical application of data structures, asynchronous programming, and automated task execution.

## ✨ Features

### 1. Smart Device Management
- Add, remove, and manage smart home devices.
- Turn individual devices on or off.
- Control devices based on their type, group, or location.
- Monitor device status, power consumption, and battery levels.

### 2. Rule-Based Automation
- Create and execute automation rules dynamically.
- Toggle devices or turn them on and off automatically.
- Control multiple devices using group, type, and location-based rules.
- Adjust device power levels through rule execution.

### 3. Intelligent Power Management
- Monitor overall power consumption.
- Apply power-reduction strategies when consumption exceeds a predefined threshold.
- Prioritize devices when deciding which devices to switch off.
- Track power consumption through dedicated logs.

### 4. Battery Management
- Monitor battery levels of battery-powered devices.
- Generate warnings when battery levels become low.
- Handle devices when their battery is depleted.

### 5. Temperature Monitoring and Control
- Monitor temperatures associated with device locations.
- Generate temperature-related alerts.
- Automatically adjust air conditioner operation based on the current temperature and configured ideal temperature.

### 6. Logging and Monitoring
- Maintain logs for informational messages, warnings, and severe events.
- Record power consumption and battery-related events.
- Retrieve log information through the application interface.

### 7. REST API
- Expose application functionality through REST endpoints.
- Support remote interaction with smart home devices.
- Retrieve device information and monitor system operations.

### 8. Asynchronous Processing
- Use asynchronous execution for supported operations.
- Improve responsiveness by allowing eligible tasks to execute without blocking the calling thread.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Java | Core application development |
| Spring Boot | Application framework and REST API |
| MongoDB | Data persistence |
| Maven | Dependency management and build automation |
| REST API | Communication with the application |
| Java Concurrency | Asynchronous task execution and concurrent operations |
| Custom Linked List | Device and task management |
| Priority Queue | Priority-based task and device management |
| ConcurrentHashMap | Thread-safe data storage |

## 🏗️ Project Architecture

The application is organized into components that separate device management, business logic, API handling, and supporting functionality.

- **Controller Layer:** Handles incoming REST API requests.
- **Service Layer:** Implements smart home operations and device management logic.
- **Device Layer:** Represents devices and their associated behavior.
- **Rule Engine:** Processes automation rules and executes corresponding actions.
- **Data Structures:** Support device collections and priority-based operations.
- **Task Management:** Handles application tasks and logging operations.
- **Persistence Layer:** Supports data storage through MongoDB.

## 📂 Project Structure

```text
Smart-Home-Automation-Java/
├── src/
│   └── main/
│       └── java/
│           └── com/
│               └── smarthome/
│                   ├── Main.java
│                   ├── SmartHome.java
│                   ├── SmartHomeApplication.java
│                   ├── SmartHomeController.java
│                   ├── config/
│                   ├── datastuctures/
│                   ├── devices/
│                   ├── enums/
│                   ├── misc/
│                   └── tasks/
├── docs/
├── pom.xml
├── LICENSE
└── README.md
```

## ⚙️ Getting Started

### Prerequisites

Ensure the following tools are installed:

- Java Development Kit (JDK)
- Apache Maven
- MongoDB, if required by your application configuration
- Git

### 1. Clone the Repository

```bash
git clone <your-repository-url>
```

Navigate to the project directory:

```bash
cd Smart-Home-Automation-Java
```

### 2. Configure the Application

Review the application configuration and update the MongoDB connection settings, if required.

Ensure the database service is running and the connection details match your local environment.

### 3. Build the Project

Run the following command:

```bash
mvn clean install
```

### 4. Run the Application

Start the Spring Boot application using:

```bash
mvn spring-boot:run
```

Alternatively, build the application and run its generated JAR file if the project is configured to package an executable Spring Boot JAR.

### 5. Access the REST API

Once the application starts, use an API client such as Postman or curl to interact with the available endpoints.

Refer to `SmartHomeController.java` for the implemented API routes and supported operations.

**Note:** The server port, endpoint paths, request formats, and database settings depend on the application configuration.

## 🧠 Concepts Demonstrated

This project demonstrates the practical application of:

- Object-Oriented Programming (OOP)
- Custom data structure implementation
- Linked lists and priority queues
- Thread-safe collections
- Asynchronous programming
- RESTful API development
- Database integration
- Rule-based automation
- Exception handling
- Logging and monitoring
- Modular software architecture

## 🚀 Future Enhancements

Potential improvements include:

- User authentication and role-based authorization.
- Integration with physical IoT devices and sensors.
- A web-based dashboard for device monitoring and control.
- Real-time updates for device status and power consumption.
- Advanced scheduling and event-driven automation.
- Integration with external smart home platforms.
- Enhanced analytics for energy consumption and device usage.

## 🎯 Project Objective

The objective of this project is to develop a modular smart home automation system that simplifies device management, supports automated decision-making, and demonstrates how Java programming, data structures, concurrency, database integration, and REST APIs can be combined to solve a practical problem.

## 📄 License

Refer to the `LICENSE` file in this repository for licensing information.
>>>>>>> 38c13ae342b97e6bc472a7d9e6b6fb186377381a
