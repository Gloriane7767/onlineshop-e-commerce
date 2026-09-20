# 🛒 Online Shop Demo

[![Java](https://img.shields.io/badge/Java-8%2B-orange.svg)](https://www.oracle.com/java/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen.svg)]()

A clean and simple Java-based online shop management system demonstrating core OOP principles with order processing, customer management, and product handling.

## ✨ Features

- 🧑‍💼 **Customer Management** - Create and manage customer profiles
- 📦 **Product Catalog** - Handle products with pricing and inventory
- 🛍️ **Order Processing** - Create orders and manage product collections
- 💰 **Price Calculation** - Automatic total calculation with quantity support
- 📊 **Order Summary** - Detailed order reporting and display

## 🏗️ Architecture

Simple 3-class design following clean architecture principles:

```
Customer ←→ Order ←→ Product
```

### Core Classes

| Class | Responsibility |
|-------|---------------|
| `Customer` | User information and validation |
| `Product` | Product details, pricing, and inventory |
| `Order` | Order management and business logic |

## 🚀 Quick Start

### Prerequisites

- Java 8 or higher
- Any IDE or text editor

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/workshop-onlineshop-demo.git
   cd workshop-onlineshop-demo
   ```

2. **Compile the project**
   ```bash
   javac src/main/java/com/gloriane/*.java
   ```

3. **Run the application**
   ```bash
   java -cp src/main/java com.gloriane.Main
   ```

## 💻 Usage

### Basic Example

```java
// Create customer
Customer customer = new Customer("John Doe", "john@example.com");

// Create order
Order order = new Order(customer);

// Create products
Product[] products = {
    new Product("Laptop", 999.99, 1),
    new Product("Mouse", 29.99, 2)
};

// Add products to order
order.addProducts(products);

// Display order summary
order.displayOrderSummary();
```

### Sample Output

```
=== ORDER DETAILS ===
Customer: John Doe
Products ordered:
- Laptop: $999.99
- Mouse: $59.98
Total items: 2
Total amount: $1059.97
```

## 📁 Project Structure

```
workshop-onlineshop-demo/
├── src/main/java/com/gloriane/
│   ├── Main.java          # Application entry point
│   ├── Customer.java      # Customer entity
│   ├── Order.java         # Order management
│   └── Product.java       # Product entity
└── README.md
```

## 🔧 API Reference

### Customer Class

```java
Customer(String name, String email)
String getName()
String getEmail()
int getId()
```

### Product Class

```java
Product(String name, double price, int quantity)
String getName()
double getPrice()
int getQuantity()
double getTotalPrice()
```

### Order Class

```java
Order(Customer customer)
void addProduct(String name, double price, int quantity)
void addProducts(Product[] products)
void removeProduct(Product product)
double getTotalPrice()
void displayOrderSummary()
```

## 🎯 Design Patterns

- **Encapsulation** - Private fields with public accessors
- **Composition** - Order contains Customer and Products
- **Validation** - Input validation in setters
- **Auto-generation** - Unique ID generation for entities

## 🛠️ Development

### Code Style
- Follow Java naming conventions
- Use meaningful variable names
- Keep methods focused and small
- Add validation for user inputs

### Testing
```bash
# Compile and run
javac src/main/java/com/gloriane/*.java
java -cp src/main/java com.gloriane.Main
```

## 🚧 Future Enhancements

- [ ] Database integration (JPA/Hibernate)
- [ ] REST API endpoints (Spring Boot)
- [ ] Shopping cart functionality
- [ ] Payment processing
- [ ] Order status tracking
- [ ] Product categories
- [ ] User authentication
- [ ] Unit tests (JUnit)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Gloriane Dev**
- GitHub: [@yourusername](https://[github.com/yourusername](https://github.com/Gloriane7767))
- Email: gloriane7767@gmail.com

## 🙏 Acknowledgments

- Built as a learning project for Java OOP concepts
- Demonstrates clean code principles
- Educational purposes only

---

⭐ **Star this repository if you found it helpful!**
