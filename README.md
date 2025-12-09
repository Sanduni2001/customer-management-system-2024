# Customer Management System

A web-based customer management system built with PHP and MySQL for efficiently managing customer information. This system provides a complete CRUD (Create, Read, Update, Delete) interface for customer data management.

## 📋 Table of Contents

- [Features](#features)
- [Technology Stack](#technology-stack)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Database Setup](#database-setup)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## ✨ Features

- **View Customers**: Display all customers in a responsive table format
- **Add Customer**: Create new customer records with validation
- **Update Customer**: Edit existing customer information
- **Delete Customer**: Remove customer records with automatic ID reordering
- **Email Validation**: Prevents duplicate email addresses
- **Responsive Design**: Mobile-friendly interface using Bootstrap 5
- **User-Friendly Interface**: Clean and intuitive UI

## 🛠 Technology Stack

- **Backend**: PHP 7.4+
- **Database**: MySQL
- **Frontend**: HTML5, CSS3, JavaScript
- **Framework**: Bootstrap 5.3.3
- **Server**: Apache/Nginx (XAMPP/WAMP/MAMP recommended)

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- PHP 7.4 or higher
- MySQL 5.7 or higher
- Apache/Nginx web server
- OR use a pre-packaged solution:
  - [XAMPP](https://www.apachefriends.org/) (Windows/Mac/Linux)
  - [WAMP](https://www.wampserver.com/) (Windows)
  - [MAMP](https://www.mamp.info/) (Mac)

## 🚀 Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/customer-management-system-2024.git
   cd customer-management-system-2024
   ```

2. **Copy files to your web server directory**

   - For XAMPP: Copy to `C:\xampp\htdocs\customer-management-system-2024` (Windows) or `/Applications/XAMPP/htdocs/customer-management-system-2024` (Mac)
   - For WAMP: Copy to `C:\wamp64\www\customer-management-system-2024`
   - For MAMP: Copy to `/Applications/MAMP/htdocs/customer-management-system-2024`

3. **Start your web server and MySQL service**

4. **Access the application**
   - Open your browser and navigate to: `http://localhost/customer-management-system-2024/customer.php`

## ⚙️ Configuration

### Database Configuration

Edit the `dbcon.php` file with your database credentials:

```php
$servername = "localhost";
$username = "root";        // Your MySQL username
$password = "root";        // Your MySQL password
$db = "possystem";         // Your database name
```

## 🗄 Database Setup

1. **Create the database**

   ```sql
   CREATE DATABASE possystem;
   ```

2. **Create the Customer table**

   ```sql
   USE possystem;

   CREATE TABLE customer (
       CustomerID INT AUTO_INCREMENT PRIMARY KEY,
       FirstName VARCHAR(50) NOT NULL,
       LastName VARCHAR(50) NOT NULL,
       Contact VARCHAR(20) NOT NULL,
       Address TEXT NOT NULL,
       Email VARCHAR(100) NOT NULL UNIQUE
   );
   ```

3. **Verify the table structure**
   ```sql
   DESCRIBE customer;
   ```

## 📖 Usage

### Viewing Customers

- Navigate to `customer.php` to see all registered customers
- The table displays Customer ID, First Name, Last Name, Contact, Address, and Email

### Adding a Customer

1. Click the "ADD Data" button on the customer list page
2. Fill in the required fields:
   - First Name
   - Last Name
   - Contact Number
   - Address
   - Email (must be unique)
3. Click "Add" to save the customer

### Updating a Customer

1. Click the "Edit Data" button next to the customer you want to update
2. Modify the information in the form
3. Click "Add" to save changes (Note: Button text should be updated to "Update")

### Deleting a Customer

1. Click the "Delete Data" button next to the customer you want to remove
2. Confirm the deletion
3. The customer will be deleted and subsequent customer IDs will be automatically reordered

## 📁 Project Structure

```
customer-management-system-2024/
│
├── addcustomer.php          # Add new customer page
├── customer.php              # Main customer listing page
├── updatecustomer.php        # Update customer information page
├── deletecustomer.php        # Delete customer functionality
├── dbcon.php                 # Database connection configuration
├── styles.css                # Custom CSS styles
└── README.md                 # Project documentation
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

- **Development Team** - Year 2 Semester 1 Information Management & Retrieval

## 🔒 Security Notes

⚠️ **Important**: This is a basic implementation for educational purposes. For production use, consider:

- Using prepared statements to prevent SQL injection
- Implementing proper authentication and authorization
- Adding input sanitization and validation
- Using HTTPS for secure data transmission
- Implementing CSRF protection
- Adding rate limiting
- Using environment variables for sensitive configuration

## 🐛 Known Issues

- The update button text says "Add" instead of "Update" (minor UI issue)
- No pagination for large customer lists
- No search/filter functionality

## 🔮 Future Enhancements

- [ ] Add search and filter functionality
- [ ] Implement pagination for customer list
- [ ] Add user authentication system
- [ ] Export customer data to CSV/Excel
- [ ] Add customer profile images
- [ ] Implement data validation on the frontend
- [ ] Add confirmation dialogs for delete operations
- [ ] Implement prepared statements for better security

---

**Note**: This project was developed as part of the Year 2 Semester 1 Information Management & Retrieval course.
