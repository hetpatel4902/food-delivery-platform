# 🍔 Food Delivery Platform

A complete food delivery ecosystem built with React Native, consisting of three interconnected mobile applications for customers, restaurant partners, and delivery partners.

The platform was developed as an end-to-end system where restaurants can manage their menus and orders, customers can discover restaurants and place orders, and delivery partners can accept and complete deliveries with location-based navigation and tracking.

The project was developed over approximately two months and focuses on building a complete real-world workflow across multiple user roles rather than a single standalone application.

## 📱 Applications

The platform consists of three separate React Native applications:

### 👤 User Application

The customer-facing application allows users to:

- Create an account and verify their email
- Log in and recover forgotten passwords
- Automatically detect their location
- Discover restaurants and available offers
- Browse restaurant menus and dishes
- View and apply restaurant-created coupons
- Add items to cart and place orders
- View order details and order history
- Track order status
- Track the delivery partner's location
- Save restaurants or dishes as favourites
- Update their delivery address

**Repository:** [Food Delivery Platform](https://github.com/hetpatel4902/food-delivery-platform)

---

### 🏪 Restaurant Partner Application

The restaurant application allows restaurant partners to manage their restaurant and fulfil customer orders.

Key capabilities include:

- Restaurant registration and authentication
- Automatic location detection
- Restaurant address management
- Create and manage dishes
- View and delete current dishes
- Upload restaurant images
- Manage incoming orders
- Update order status during preparation
- View completed order history

**Repository:** [Restaurant Partner App](https://github.com/hetpatel4902/food-delivery-restaurant-app)

---

### 🛵 Delivery Partner Application

The delivery application allows delivery partners to manage available deliveries and navigate between restaurants and customers.

Key capabilities include:

- Delivery partner authentication
- View available orders
- Accept delivery requests
- View delivery distance and estimated travel information
- Navigate to the restaurant
- Navigate from the restaurant to the customer
- Share delivery location for customer tracking
- Complete deliveries after reaching the destination

**Repository:** [Delivery Partner App](https://github.com/hetpatel4902/food-delivery-delivery-app)

## 🎥 Demo

A combined demonstration of the three applications is available, showing the end-to-end food delivery workflow across the customer, restaurant partner, and delivery partner applications.

The demonstration covers the interaction between the three applications, including restaurant operations, order placement, order acceptance, delivery assignment, navigation, and delivery tracking.

Video link - https://lnkd.in/p/gjuX5eZr

## 🔄 End-to-End Order Workflow

The platform connects the three applications through a common order lifecycle:

```text
Customer
   │
   │ Places Order
   ▼
Restaurant Partner
   │
   │ Accepts & Prepares Order
   ▼
Delivery Partner
   │
   │ Accepts Delivery
   ▼
Restaurant
   │
   │ Picks Up Order
   ▼
Customer
   │
   │ Receives Order
   ▼
Order Completed
```

The delivery workflow also uses location and map-based functionality to guide the delivery partner from the current location to the restaurant and then from the restaurant to the customer.

## ✨ Key Features

### Customer Experience

- Email-based account verification
- Login and password recovery
- Automatic location detection
- Restaurant and dish discovery
- Offers and coupons
- Cart management
- Order placement
- Order status tracking
- Delivery partner location tracking
- Order history
- Favourites
- Address management

### Restaurant Operations

- Restaurant registration and authentication
- Restaurant profile and address management
- Dish creation and management
- Restaurant image uploads
- Order management
- Order status updates
- Completed order history

### Delivery Operations

- Delivery partner authentication
- Available order discovery
- Delivery acceptance
- Distance and estimated travel information
- Map-based navigation
- Restaurant-to-customer navigation
- Delivery location sharing
- Order completion

## 📍 Location & Delivery Tracking

Location-based functionality is a core part of the platform.

The delivery workflow uses the delivery partner's current location together with map and routing functionality to support navigation between the delivery partner, restaurant, and customer.

The customer application can also display the delivery partner's location during an active delivery, providing visibility into the delivery process.

## 🔐 Authentication

The applications use AWS Cognito through AWS Amplify for authentication-related functionality.

The customer application supports:

- User registration
- Email verification
- Login
- Forgot-password workflow

The restaurant and delivery applications also include authentication flows appropriate to their respective user roles.

## ☁️ Cloud & Backend Integration

The applications were designed around AWS-backed services and mobile application integrations.

The project uses AWS Amplify and Amazon Cognito for authentication and cloud integration. The applications also integrate location, mapping, and other platform services required for the food delivery workflow.

The customer application additionally integrates Stripe's React Native SDK for payment-related functionality.

## 🛠️ Technology Stack

### Mobile Development

- React Native
- JavaScript
- React Navigation

### Cloud & Authentication

- AWS Amplify
- Amazon Cognito

### Location & Maps

- React Native Maps
- Expo Location
- Google Maps / Places integration

### Payments

- Stripe

### Application Services

- AsyncStorage
- Network connectivity monitoring
- Native device capabilities

## 🏗️ Platform Architecture

The overall platform can be viewed as three role-specific mobile clients working together through shared backend and cloud services.

```text
                         FOOD DELIVERY PLATFORM
                                  │
              ┌───────────────────┼───────────────────┐
              │                   │                   │
              ▼                   ▼                   ▼
        User Application   Restaurant Application  Delivery Application
              │                   │                   │
              └───────────────────┼───────────────────┘
                                  │
                                  ▼
                         Cloud / Backend Services
                                  │
                    ┌─────────────┼─────────────┐
                    │             │             │
                    ▼             ▼             ▼
                 Cognito      Data Services   Storage
                    │
                    ▼
              Authentication
```

The individual applications are maintained in separate repositories:

- [User Application](https://github.com/hetpatel4902/food-delivery-platform)
- [Restaurant Partner Application](https://github.com/hetpatel4902/food-delivery-restaurant-app)
- [Delivery Partner Application](https://github.com/hetpatel4902/food-delivery-delivery-app)

## 📁 Repository Structure

The project is organized into three repositories based on user roles:

```text
Food Delivery Platform
│
├── food-delivery-platform
│   └── User Application
│
├── food-delivery-restaurant-app
│   └── Restaurant Partner Application
│
└── food-delivery-delivery-app
    └── Delivery Partner Application
```

## 🚀 Getting Started

Each application is maintained as a separate React Native project.

### Prerequisites

- Node.js
- React Native development environment
- Android Studio and/or Xcode
- Android/iOS device or emulator
- Required AWS configuration
- Required map service configuration

### User Application

```bash
git clone https://github.com/hetpatel4902/food-delivery-platform.git
cd food-delivery-platform
npm install
npx react-native start
```

Run the application using the React Native Android or iOS tooling.

### Restaurant Partner Application

```bash
git clone https://github.com/hetpatel4902/food-delivery-restaurant-app.git
cd food-delivery-restaurant-app
npm install
npx react-native start
```

### Delivery Partner Application

```bash
git clone https://github.com/hetpatel4902/food-delivery-delivery-app.git
cd food-delivery-delivery-app
npm install
npx react-native start
```

> Note: The applications depend on external cloud services and platform-specific configuration. Additional environment and service configuration may be required before running the complete workflow.

## 📌 Project Background

This project was developed as an exploration of building a complete multi-role food delivery ecosystem rather than a single mobile application.

The project required designing and implementing three separate applications that represent different participants in the same business workflow: customers, restaurant partners, and delivery partners.

The project was developed over approximately two months and provided hands-on experience with mobile application development, authentication, cloud services, location-based functionality, maps, navigation, payment integration, and multi-application workflows.

## 🔗 Related Repositories

- 👤 [User / Main Platform](https://github.com/hetpatel4902/food-delivery-platform)
- 🏪 [Restaurant Partner App](https://github.com/hetpatel4902/food-delivery-restaurant-app)
- 🛵 [Delivery Partner App](https://github.com/hetpatel4902/food-delivery-delivery-app)
