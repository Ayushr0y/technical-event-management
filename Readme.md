# Technical Event Management System

A beautiful, modern Flask-based event management system with role-based access control and stunning UI/UX design.

## ✨ Features

- **Beautiful Modern Design** - Gradient backgrounds, smooth animations, and responsive layouts
- **Three User Roles** - Admin, Vendor, and User with unique color themes
- **Session-Based Authentication** - Secure login with hidden passwords
- **Maintenance Module** - Admin-only vendor and user management
- **Transaction Module** - Vendors add items, Users request items
- **Reports Module** - Comprehensive order tracking and status updates
- **Fully Responsive** - Works perfectly on desktop, tablet, and mobile devices

## 🎨 Design Highlights

- **Role-Based Color Schemes**
  - Admin: Purple gradient theme
  - Vendor: Pink gradient theme
  - User: Teal/Pink gradient theme
  
- **Smooth Animations**
  - Page load animations
  - Hover effects
  - Particle effects on landing page
  - Status badge animations
  
- **Modern Typography**
  - Google Poppins font
  - Multiple weight variations
  - Responsive font sizes

For complete design documentation, see [DESIGN_FEATURES.md](DESIGN_FEATURES.md)

## Folder Structure

```
event_management/
├── app.py
├── event_management.db (created automatically)
├── templates/
│   ├── index.html
│   ├── login.html
│   ├── admin_dashboard.html
│   ├── maintain_vendor.html
│   ├── maintain_user.html
│   ├── membership.html
│   ├── admin_reports.html
│   ├── vendor_dashboard.html
│   ├── add_item.html
│   ├── vendor_items.html
│   ├── user_dashboard.html
│   ├── request_item.html
│   └── user_orders.html
└── README.md
```

## Installation

1. Install Flask:
```
pip install flask
```

2. Run the application:
```
python app.py
```

3. Open browser and go to:
```
http://127.0.0.1:5000
```

## Default Login Credentials

**Admin:**
- Username: admin
- Password: admin123
- Role: Admin

## How to Use

### Admin:
1. Login with admin credentials
2. Maintain Vendor - Add or Update vendors
3. Maintain User - Add or Update users
4. Membership Management - Add or Update memberships with duration options
5. View Order Status Report - See all transactions

### Vendor:
1. Get login credentials from Admin
2. Login with vendor role
3. Add items to the system
4. View all your items

### User:
1. Get login credentials from Admin
2. Login with user role
3. Request items from available items
4. View your order status

## Database Tables

- users (id, username, password, role, email, phone, address, created_at)
- vendors (id, username, password, company_name, email, phone, address, created_at)
- memberships (id, user_id, duration, start_date, end_date, status)
- items (id, vendor_id, item_name, description, price, quantity, created_at)
- transactions (id, user_id, item_id, vendor_id, quantity, total_price, status, request_date)

## Notes

- All fields are mandatory
- Radio buttons allow only one selection
- Passwords are hidden in input fields
- Session management for secure login
- Role-based access control