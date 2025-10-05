<div align="center">

# Cafe POS - Restaurant Management System

[![Java](https://img.shields.io/badge/Java-17-orange.svg)](https://www.oracle.com/java/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-blue.svg)](https://www.mysql.com/)
[![Swing](https://img.shields.io/badge/GUI-Java%20Swing-green.svg)](https://docs.oracle.com/javase/tutorial/uiswing/)
[![NetBeans](https://img.shields.io/badge/IDE-NetBeans-blue.svg)](https://netbeans.apache.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

</div>

A comprehensive Point of Sale (POS) and Restaurant Management System built with Java Swing, featuring modern UI design, complete inventory management, and powerful reporting capabilities.

## Screenshots

### Dashboard & Analytics

![Dashboard](cafe/screenshots/dashboard.png)

### Login & Authentication

![Login](cafe/screenshots/login.png)

### Menu & Category Management

![Menu Management](cafe/screenshots/menu_management.png)
![Category Management](cafe/screenshots/manage_categories.png)

### Sales & Orders

![Sales Channel](cafe/screenshots/sales_channel.png)
![Pre Orders](cafe/screenshots/pre_orders.png)

### Inventory Management

![Supplier Management](cafe/screenshots/supplier_management.png)
![Purchase Orders](cafe/screenshots/purchase_order.png)
![GRN (Goods Receipt Note)](cafe/screenshots/grn.png)
![Damaged Stock](cafe/screenshots/damaged_stock.png)

### Customer & Table Management

![Customer Management](cafe/screenshots/customer_management.png)
![Table Management](cafe/screenshots/table_management.png)
![Reservations](cafe/screenshots/reservations.png)

### Reports & Analytics

![Analytics & Reports](cafe/screenshots/analytics_and_reports.png)

### User & System Management

![User Management](cafe/screenshots/user_management.png)
![User Activity](cafe/screenshots/user_activity.png)
![Settings](cafe/screenshots/settings.png)

### Discounts & Promotions

![Discounts](cafe/screenshots/discounts.png)

## Features

### Core POS Functionality

- **Multi-Channel Sales**: Dine-in, Takeaway, and Pre-order management
- **Table Management**: Dynamic table allocation and reservation system
- **Order Processing**: Real-time order tracking and kitchen management
- **Invoice Generation**: Professional PDF invoice creation with JasperReports

### Inventory & Stock Management

- **Real-time Stock Tracking**: Automatic inventory updates with each sale
- **Kitchen Stock Management**: Separate inventory for kitchen items
- **Damage Stock Tracking**: Monitor and record damaged goods
- **Low Stock Alerts**: Automated notifications for limited stock items
- **Supplier Management**: Complete supplier database and purchase orders

### User & Access Management

- **Role-based Access Control**: Admin, Manager, and Staff roles
- **User Activity Logging**: Comprehensive audit trail
- **Secure Authentication**: Token-based user sessions
- **User Registration**: Easy staff onboarding system

### Analytics & Reporting

- **Sales Dashboard**: Real-time sales metrics and charts
- **Financial Reports**: Revenue, profit, and expense tracking
- **Inventory Reports**: Stock levels and movement analysis
- **Custom Date Ranges**: Flexible reporting periods
- **Visual Charts**: Interactive charts using JFreeChart

### Modern UI/UX

- **FlatLaf Theme System**: Modern, customizable interface
- **Dark/Light Mode**: Multiple theme options
- **Responsive Design**: Optimized for different screen sizes
- **Custom Components**: Beautiful cards and interactive elements

### Advanced Features

- **Discount Management**: Flexible discount rules and promotions
- **Category Management**: Hierarchical menu organization
- **Customer Registration**: Customer database and loyalty tracking
- **Backup & Restore**: Database backup functionality
- **Multi-language Support**: Expandable localization system

## Technology Stack

### Backend

- **Java 17**: Core application logic
- **MySQL 8.1**: Primary database
- **JDBC**: Database connectivity

### Frontend

- **Java Swing**: GUI framework
- **FlatLaf 3.1.1**: Modern Look and Feel
- **JFreeChart 1.5.4**: Data visualization
- **JCalendar**: Date picker components

### Libraries & Dependencies

- **JasperReports 6.20.5**: Professional report generation
- **OpenPDF 1.3.30**: PDF document creation
- **MySQL Connector 8.1.0**: Database driver
- **Commons Collections**: Utility libraries
- **Groovy**: Scripting support

## Installation

### Prerequisites

- Java Development Kit (JDK) 17 or higher
- MySQL Server 8.0 or higher
- NetBeans IDE (recommended) or any Java IDE

### Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/gitxar7/RestuarantManagementSystem.git
   cd RestuarantManagementSystem
   ```

2. **Database Setup**

   ```sql
   -- Create database
   CREATE DATABASE cafe_db_new;

   -- Import the database schema
   mysql -u root -p cafe_db_new < database/cafe_schema.sql
   ```

3. **Configure Database Connection**

   Update the database credentials in `src/com/cafe/model/Mysql.java`:

   ```java
   private static String user = "your_username";
   private static String password = "your_password";
   ```

4. **Build and Run**

   ```bash
   # Using NetBeans
   # Open project in NetBeans and run

   # Or using command line
   ant clean compile jar
   java -jar dist/cafe.jar
   ```

## Project Structure

```
cafe/
├── src/com/cafe/
│   ├── gui/           # User Interface Components
│   │   ├── Dashboard.java
│   │   ├── MenuManagement.java
│   │   ├── StockManagement.java
│   │   └── ...
│   ├── model/         # Data Models & Database
│   │   ├── Mysql.java
│   │   ├── User.java
│   │   ├── MenuItem.java
│   │   └── ...
│   ├── reports/       # JasperReports Templates
│   ├── style/         # Custom UI Styling
│   └── img/           # Application Images
├── lib/               # External JAR Dependencies
├── build/             # Compiled Classes
└── nbproject/         # NetBeans Project Files
```

## Usage

### Getting Started

1. **Login**: Use default admin credentials or create new user
2. **Setup Menu**: Add categories and menu items
3. **Configure Stock**: Initialize inventory levels
4. **Start Selling**: Process orders through POS interface

### Key Workflows

**Processing an Order:**

1. Select dining option (Dine-in/Takeaway)
2. Choose menu items and quantities
3. Apply discounts if applicable
4. Generate invoice and process payment

**Managing Inventory:**

1. Navigate to Stock Management
2. Add new stock or update existing
3. Set minimum stock levels for alerts
4. Generate stock reports

**Viewing Reports:**

1. Access Reports section
2. Select report type and date range
3. Generate PDF or view on screen
4. Export data for external analysis

## Configuration

### Theme Customization

Modify themes in `src/com/cafe/style/`:

- `CustomStyle.java`: Custom component styling
- `Pallet.java`: Color schemes and palettes

### Database Configuration

Update connection settings in `src/com/cafe/model/Mysql.java`:

- Database URL
- Username and password
- Connection parameters

### Report Templates

Customize reports in `src/com/cafe/reports/`:

- Invoice templates
- Sales reports
- Inventory reports

## Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines

- Follow Java naming conventions
- Add comments for complex logic
- Test new features thoroughly
- Update documentation as needed

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Future Enhancements

- [ ] **Cloud Integration**: Online synchronization and backup
- [ ] **Mobile App**: Complementary mobile application
- [ ] **Payment Gateway**: Integration with popular payment processors
- [ ] **Analytics Dashboard**: Advanced business intelligence
- [ ] **Multi-location Support**: Chain restaurant management
- [ ] **API Development**: RESTful API for third-party integrations

## Support

For support and questions:

- **Developer**: Abdur Rahman Hanas
- **Email**: nxt.genar7@gmail.com
- **Issues**: [GitHub Issues](https://github.com/gitxar7/RestuarantManagementSystem/issues)
- **Documentation**: [Wiki](https://github.com/gitxar7/RestuarantManagementSystem/wiki)

## Acknowledgments

- **FlatLaf**: For the modern Look and Feel
- **JFreeChart**: For powerful charting capabilities
- **JasperReports**: For professional report generation
- **MySQL**: For reliable database management
- **Apache Commons**: For utility libraries

---

<div align="center">
  <b>Built by Abdur Rahman Hanas and the Team</b>
  <br>
  <sub>Star this repository if you found it helpful!</sub>
</div>
