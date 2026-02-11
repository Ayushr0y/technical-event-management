# Technical Event Management System

A Flask-based Technical Event Management System with role-based access control.

## Features

- Clean and responsive user interface
- Three User Roles: Admin, Vendor, and User
- Session-based authentication with hidden password fields
- Maintenance Module (Admin only)
- Transaction Module (Vendor adds items, User requests items)
- Reports Module for order tracking and status updates
- Role-based access control

## Interface

- Role-based dashboards
- Simple navigation between modules
- Basic responsive layout

## Folder Structure

event_management/
├── app.py
├── event_management.db (created automatically)
├── templates/
│ ├── index.html
│ ├── login.html
│ ├── admin_dashboard.html
│ ├── maintain_vendor.html
│ ├── maintain_user.html
│ ├── membership.html
│ ├── admin_reports.html
│ ├── vendor_dashboard.html
│ ├── add_item.html
│ ├── vendor_items.html
│ ├── user_dashboard.html
│ ├── request_item.html
│ └── user_orders.html
└── README.md

## Installation

1. Install Flask:
pip install flask

2. Run the application:
python app.py

3. Open browser and go to:
http://127.0.0.1:5000

## Default Login Credentials

Admin:
Username: admin  
Password: admin12  
Role: admin  

## How to Use

### Admin:
1. Login with admin credentials
2. Maintain Vendor - Add or Update vendors
3. Maintain User - Add or Update users
4. Membership Management - Add or Update memberships
5. View Order Status Report

### Vendor:
1. Get login credentials from Admin
2. Login with vendor role
3. Add items
4. View your items

### User:
1. Get login credentials from Admin
2. Login with user role
3. Request available items
4. View your order status

## Database Tables

- users
- vendors
- memberships
- items
- transactions

## Notes

- All required fields are validated
- Radio buttons allow only one selection
- Passwords are hidden in login forms
- Session management is implemented
- Role-based access is enforced
