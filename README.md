# skill-link-fyp
Skill-Link – A Student Skill Sharing and Gig Marketplace Platform
Skill-Link is a full-stack MERN web application designed to connect verified university students with clients who need affordable and trustworthy freelance services. The system is built according to the Software Requirements Specification (SRS) provided in docs/SRS.md.

It includes mandatory .edu.pk email verification, an escrow-based payment system, real-time chat, digital PDF receipts, ratings and reviews, dispute handling, and a complete admin panel for platform management.

📑 Table of Contents
Project Overview
Core Features
Technology Stack
Architecture
Folder Structure
Quick Start Guide
Demo Accounts
Demo Workflow
Testing
API Reference
Database Design
Student Verification Rules
Environment Variables
Deployment Guide
Troubleshooting
FYP Evaluation Checklist
License & Credits
🧩 1. Project Overview

Skill-Link is a student-focused freelance marketplace where verified university students can offer services (gigs) to clients.

The platform is designed to ensure trust, transparency, and secure transactions through the following key principles:

Student Verification: Only users with .edu.pk email addresses can register as freelancers. Additionally, an ID-card verification system is included for extra validation.
Escrow Payments: Client payments are held securely in escrow and released only after order approval. In case of disputes, an admin can intervene.
Real-Time Communication: A Socket.io-based chat system allows instant messaging between client and freelancer during active orders.
Professional Marketplace: Users can build profiles, upload portfolios, receive ratings, generate PDF receipts, and manage orders efficiently.

The system fully implements all SRS requirements and includes automated testing and end-to-end validation scripts to ensure reliability and correctness.

⚙️ 2. Core Features
🔐 Authentication & Security
Email/password registration and login (JWT-based)
Email verification and password reset
Role-based access control (Student, Client, Admin)
Rate limiting and disposable email blocking
🎓 Student Verification
Mandatory .edu.pk email restriction
Optional university whitelist
ID card upload and admin approval system
💼 Gigs System
Create, update, delete gigs
Search, filter, and sort by skill, price, and rating
Image support for gig previews
📦 Orders System
Place orders and track progress
Escrow-based workflow (fund → deliver → approve → complete)
Dispute handling and admin resolution
💳 Payments
Stripe integration (test mode)
Secure escrow payment handling
PDF invoice generation using PDFKit
💬 Real-Time Chat
Socket.io messaging system
Order-based chat rooms
Message history and authorization control
⭐ Reviews & Ratings
1–5 star rating system
Reviews only allowed after order completion
Automatic rating aggregation
🔔 Notifications
In-app notifications for order updates
Real-time updates for key events
🛠️ Admin Panel
User management (ban/activate/deactivate)
Verification approvals
Dispute resolution
Platform analytics dashboard
🏗️ 3. Technology Stack

Frontend: React, Vite, Tailwind CSS, Axios, Socket.io-client
Backend: Node.js, Express.js, Mongoose, JWT, Socket.io
Database: MongoDB (Atlas or local Docker)
Testing: Jest, Supertest, MongoDB Memory Server
Payments: Stripe API
Email: Nodemailer

🧠 4. Architecture

The system follows a modern client-server architecture:

React frontend communicates with Express backend via REST APIs
Socket.io handles real-time communication
MongoDB stores persistent data
Stripe manages secure payment flow
📂 5. Folder Structure

The project is organized into:

backend/ → API, models, controllers, routes, services
frontend/ → React UI, pages, components
docs/ → SRS and documentation
scripts/ → Testing and automation tools
🚀 6. Quick Start
Clone repository
Start MongoDB
Install backend dependencies
Run backend server
Install frontend dependencies
Start frontend server
Open browser at localhost:5173
👤 7. Demo Accounts
Admin: admin@skill-link.local
Student: asad@nust.edu.pk
Client: client@example.com
🔄 8. Demo Workflow
Client browses gigs and places an order
Escrow payment is created
Student delivers work
Client approves and releases payment
Review is submitted
Admin monitors system activity
🧪 9. Testing

The project includes:

Unit tests
Integration tests
End-to-end workflow validation

All major user flows are automatically verified.

🌐 10. Deployment
Backend: Render / Railway
Frontend: Vercel / Netlify
Database: MongoDB Atlas
Optional: Docker for full-stack deployment
⚠️ 11. Troubleshooting

Common issues include:

Rate limiting during signup
Missing SMTP configuration
MongoDB connection errors
CORS issues in frontend
🎯 12. Evaluation Checklist

The system fulfills all FYP requirements including:

Authentication system
Student verification
Escrow payment workflow
Real-time chat
Admin control panel
Full CRUD operations
Security implementation
Testing coverage
📜 13. License

This project is submitted as a Final Year Project (FYP) and is intended for academic evaluation and learning purposes.
