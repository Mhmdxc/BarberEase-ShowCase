# 💈 BarberEase: A Real-Time Appointment & Booking System

[▶️ **Watch the Video Walkthrough**](https://vimeo.com/1097529578/c4564b2a8e?share=copy)  
*(The video is the best way to see the project in action!)*

---

🚀 **BarberEase** is a full-stack, real-time appointment booking and management platform designed for modern barbershops. The system enables clients to book slots in real time, while providing barbers and admins with a powerful dashboard for managing schedules, business logic, and asynchronous workflows.

![BarberEase Homepage Hero Image](https://github.com/Mhmdxc/BarberEase-Showcase/blob/main/assets/home.jpg?raw=true)

---

## 🧠 Project Motivation

This project was inspired by real-world scheduling inefficiencies observed at a local barbershop. It was developed from scratch to digitize the booking process, reduce manual overhead, and provide a scalable, professional solution that mirrors SaaS-level product quality.

---

## ⚙️ Tech Stack

| Layer         | Technology                     |
|--------------|---------------------------------|
| **Frontend** | HTML5, Tailwind CSS, JavaScript |
| **Backend**  | Laravel (PHP 8+), Laravel Sail (Docker) |
| **Database** | MySQL                           |
| **Auth**     | Laravel Sanctum (SPA-compatible API auth) |
| **Real-Time**| Laravel Reverb, Laravel Echo, WebSockets |
| **Async**    | Laravel Queues (database driver) |
| **Testing**  | PestPHP (Feature + Unit Testing) |
| **DevOps**   | Docker-based local development with Sail |

---

## ✨ Highlight Features

### 🌐 Real-Time & Event-Driven Core

- **🔄 Live Slot Availability**: Powered by Laravel Reverb and WebSockets, all booking updates propagate instantly across all connected clients, preventing double-bookings.
- **🔔 Context-Aware Notifications**: An event-driven notification system alerts users and admins in real-time about relevant actions like approvals or cancellations. This is handled by **Laravel's Queue System** for a non-blocking user experience.

### 🔌 API-First Architecture

- **🌐 Stateless RESTful API**: All core functionalities are exposed via a secure, versioned API, making the application ready for any future client, such as a native mobile app.
- **🔑 Token-Based Authentication**: API endpoints are protected using **Laravel Sanctum**, providing a modern and secure authentication method for single-page applications or mobile clients.

### 💇‍♂️ Client Experience

- **📆 Personalized Dashboard**: Authenticated users have a central dashboard to view and manage their upcoming appointments.
- **🛡️ Self-Service Management**: Clients can book and cancel their own appointments, with actions governed by **Laravel Policies** to ensure they can only modify their own data.

### 🛠️ Admin & Barber Tools

- **📋 Comprehensive Management Dashboard**: A central dashboard allows admins to view and manage all pending and approved appointments chronologically.
- **✅ Approval Workflow**: Barbers can manually approve or cancel bookings, which triggers the event-driven notification system.
- **⛔ Dynamic Business Rules**: Admins can configure core business logic—such as work hours and unavailable time blocks—from a dedicated settings panel.

---

## 🧪 Testing Strategy

The application includes targeted unit and feature tests to ensure critical booking logic and role-based access behaviors are functioning correctly.

- ✅ **Feature Testing**: Verify key user flows such as booking available appointments, preventing bookings in the past, avoiding double-bookings, and restricting access for unauthenticated users.
- 🧪 **Unit Testing**: Focus on validating time-slot availability logic within the `SlotService`, including detection of slots outside business hours.
- 🎭 **Mocking/Faking**: Events such as `AppointmentUpdated` and `SlotUpdated` are faked to isolate logic and ensure correct triggering without external dependencies.

---

## 🏗️ Architectural Design

This project adheres to scalable, production-ready design patterns:

- **📐 MVC Pattern**: Clean separation of logic using Laravel’s MVC.
- **📦 Service-Oriented Architecture (SOA)**: Core logic lives in dedicated service classes, promoting reusability and testability.
- **🧵 Event-Driven System**: Leverages Laravel’s Events & Listeners for decoupled communication (e.g., appointment status → notify client).
- **⏱️ Asynchronous Jobs**: Notifications and time-intensive tasks handled via Laravel Queues.
- **🧠 Centralized Validation**: Custom Form Request classes enforce input sanitization, validation, and access control.
- **🔌 API-Ready Endpoints**: Built with RESTful APIs and Sanctum, making the app suitable for future SPA or mobile extensions.
- **🚀 Optimized for Performance**: File caching enabled, with easy migration path to Redis or Memcached.
- **🔐 Secure by Design**: CSRF protection, password hashing, and role-based access checks are implemented out-of-the-box.
- **🧱 ORM Best Practices**: Eloquent Models follow Single Responsibility and use custom query scopes for reusable filters.

---

## 🎥 See It In Action

<p align="center">
  <a href="https://vimeo.com/1097529578/c4564b2a8e?share=copy">
    <img src="https://github.com/Mhmdxc/BarberEase-Showcase/blob/main/assets/thumbnail.jpg?raw=true" alt="BarberEase Video Walkthrough">
  </a>
</p>
<p align="center"><em>Click above for a full walkthrough.</em></p>

---

## 🔒 Source Code Access

The source code for this project is **private**, but is available for review upon request. Please feel free to reach out for a technical discussion or a code walkthrough.
