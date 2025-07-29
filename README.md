# Sparkz Hotelo - Hotel Management System

![Sparkz Hotelo Logo](assets/img/logo.png)

## Project Overview

Sparkz Hotelo is a comprehensive web-based Hotel Management System designed to streamline hotel operations including room management, reservations, staff management, customer complaints, and financial tracking. This system provides an intuitive dashboard for hotel managers to efficiently handle day-to-day operations.

## 🚀 Features

### Core Functionality
- **User Authentication**: Secure login system with session management
- **Dashboard Analytics**: Real-time statistics and earnings tracking
- **Room Management**: Complete room booking, check-in/check-out system
- **Reservation System**: Customer booking management with payment tracking
- **Staff Management**: Employee records, shift management, and salary tracking
- **Complaint System**: Customer complaint registration and management
- **Financial Tracking**: Income monitoring and pending payment management

### Dashboard Metrics
- Total Rooms
- Active Reservations
- Staff Count
- Customer Complaints
- Booked Rooms
- Available Rooms
- Checked-in Guests
- Pending Payments
- Total Earnings

## 🛠️ Technology Stack

### Backend Technologies
- **PHP**: Server-side scripting language
- **MySQL**: Database management system
- **Apache**: Web server (via XAMPP)

### Frontend Technologies
- **HTML5**: Markup language
- **CSS3**: Styling and layout
- **JavaScript**: Client-side interactivity
- **jQuery**: JavaScript library for DOM manipulation
- **Bootstrap**: Responsive CSS framework
- **AJAX**: Asynchronous data exchange

### Database
- **MySQL Database**: `sparkz`
- **Connection**: `localhost` with `root` user

## 📁 Project Structure

```
sparkz/
├── 📄 Main Application Files
│   ├── index.php              # Main application router
│   ├── login.php              # User authentication page
│   ├── dashboard.php          # Main dashboard with analytics
│   ├── room_mang.php          # Room management interface
│   ├── reservation.php        # Booking and reservation system
│   ├── staff_mang.php         # Staff management interface
│   ├── add_emp.php            # Employee addition form
│   ├── complain.php           # Complaint management system
│   ├── statistics.php         # Statistical reports
│   ├── emp_history.php        # Employee history tracking
│   ├── ajax.php               # AJAX request handler
│   ├── logout.php             # Session termination
│   └── notification.php       # Notification system
│
├── 🗄️ Database Configuration
│   ├── db.php                 # Database connection
│   ├── db_connect.php         # Alternative DB connection
│   └── functionmis.php        # Additional functions
│
├── 📊 Actions (Database Queries)
│   ├── avrooms-count.php      # Available rooms count
│   ├── bookedroom-count.php   # Booked rooms count
│   ├── checkedin-count.php    # Checked-in guests count
│   ├── complaints-count.php   # Complaints count
│   ├── income-count.php       # Total income calculation
│   ├── pendingpay-count.php   # Pending payments count
│   ├── pendingpayment.php     # Pending payment details
│   ├── reserve-count.php      # Reservation count
│   ├── room-count.php         # Total rooms count
│   └── staff-count.php        # Staff count
│
├── 🎨 Assets
│   ├── css/                   # Stylesheets
│   │   ├── bootstrap.min.css
│   │   ├── font-awesome.min.css
│   │   ├── styles.css
│   │   ├── login.css
│   │   └── icons.css
│   ├── js/                    # JavaScript files
│   │   ├── jquery-1.11.1.min.js
│   │   ├── bootstrap.min.js
│   │   ├── ajax.js            # Custom AJAX functions
│   │   └── custom.js
│   ├── img/                   # Images and icons
│   └── fonts/                 # Font files
│
└── 📋 Includes
    ├── header.php             # Common header template
    ├── sidebar.php            # Navigation sidebar
    └── footer.php             # Common footer template
```

## 🔧 Installation & Setup

### Prerequisites
- XAMPP (Apache + MySQL + PHP)
- Web browser
- Text editor (optional)

### Installation Steps

1. **Download and Install XAMPP**
   ```bash
   # Download XAMPP from https://www.apachefriends.org/
   # Install and start Apache and MySQL services
   ```

2. **Clone/Copy Project Files**
   ```bash
   # Copy project files to XAMPP htdocs directory
   cp -r sparkz/ C:/xampp/htdocs/
   ```

3. **Database Setup**
   - Open phpMyAdmin (http://localhost/phpmyadmin)
   - Create a new database named `sparkz`
   - Import the database schema (if provided)
   - Configure database connection in `db.php`:
   ```php
   $connection = mysqli_connect("localhost","root","","sparkz");
   ```

4. **Access Application**
   ```
   http://localhost/sparkz
   ```

## 🎯 How It Works

### Application Flow

1. **Authentication**: Users access the system through `login.php`
2. **Routing**: `index.php` acts as the main router, directing users to different modules
3. **Dashboard**: After login, users see the main dashboard with real-time statistics
4. **Module Navigation**: Users can access different features through the sidebar navigation

### Key Components

#### 1. User Management
- Session-based authentication
- User profile management
- Role-based access (Manager role)

#### 2. Room Management System
- Add/Edit/Delete rooms
- Room type categorization
- Real-time availability status
- Check-in/Check-out processes

#### 3. Reservation System
- Customer booking interface
- Payment status tracking
- Booking history management
- Room assignment

#### 4. Staff Management
- Employee registration
- Shift management
- Salary tracking
- Performance monitoring

#### 5. Financial Tracking
- Income calculation from completed bookings
- Pending payment monitoring
- Revenue analytics

### Database Architecture

The system uses several interconnected tables:
- `user` - System users and authentication
- `room` - Room information and availability
- `room_type` - Room categories and pricing
- `booking` - Reservation and payment records
- `staff` - Employee information
- `staff_type` - Job categories
- `shift` - Work shift details
- `complaints` - Customer complaint records

### AJAX Integration

The system heavily uses AJAX for:
- Real-time form submissions
- Dynamic content loading
- Live data updates without page refresh
- Modal dialog interactions

## 🔐 Security Features

- **Session Management**: Secure user sessions
- **SQL Injection Protection**: Parameterized queries (needs improvement)
- **Access Control**: Login-required pages
- **Password Encryption**: MD5 hashing (should be upgraded to bcrypt)

## 📱 Responsive Design

- Bootstrap-based responsive layout
- Mobile-friendly interface
- Cross-browser compatibility
- Adaptive dashboard widgets

## 🌟 Key Features Breakdown

### Dashboard Analytics
- Real-time business metrics
- Visual representation of hotel statistics
- Quick access to critical information

### Room Management
- Complete room lifecycle management
- Status tracking (Available/Booked/Occupied)
- Room type management with pricing

### Booking System
- Customer information capture
- Payment processing integration
- Booking confirmation system

### Staff Operations
- Employee onboarding
- Shift scheduling
- Salary management

## 🔧 Technical Highlights

- **MVC-like Structure**: Separation of concerns with includes
- **Database Abstraction**: Centralized database connections
- **AJAX-driven**: Modern web application feel
- **Modular Design**: Easy to extend and maintain
- **Bootstrap Integration**: Professional UI/UX

## 📈 Future Enhancements

- Enhanced security with password hashing
- Payment gateway integration
- Email notification system
- Advanced reporting features
- Mobile application
- Multi-language support
- API development

## 👨‍💻 Developer Information

**Project Created By**: Nikhil Bhalerao  
**Role**: Freelancer from India  
**Contact**: ndbhalerao91@gmail.com  
**WhatsApp**: +919423979339  
**Website**: https://nikhilbhalerao.com/

## 📄 License

This project is developed as a hotel management solution. For commercial use or modifications, please contact the developer.

## 🤝 Support

For technical support, feature requests, or project development:
- Email: ndbhalerao91@gmail.com
- Telegram: @ndbhalerao91
- WhatsApp: +919423979339

---

*Sparkz Hotelo - Streamlining Hotel Operations with Modern Web Technology*
