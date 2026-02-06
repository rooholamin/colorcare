# ColorCare Platform

## Overview

This repository contains the complete source code for the **ColorCare platform**, including the backend system, web application, and mobile applications for end users and service providers.

The platform is designed as a centralized, API-driven system where all client applications communicate with a shared backend through secure RESTful interfaces.

---

## Repository Structure
.
├── web/
│   └── Laravel backend and web application
│
├── user_app/
│   └── Flutter mobile application for end users
│
├── provider_app/
│   └── Flutter mobile application for service providers
│
└── README.md
---

## Components

### 1. Web (Backend & Web Application)

**Path:** `/web`

This directory contains the backend application implemented using **Laravel**.  
It serves as the core of the ColorCare platform and provides RESTful APIs consumed by all client applications.

**Responsibilities:**
- Business logic and domain services
- Authentication and authorization
- Booking and service workflows
- Data persistence and transactions
- Background job processing
- API endpoints for web and mobile clients

**Primary Technologies:**
- Laravel 12
- PHP 8.5
- MySQL
- Redis
- Nginx (deployment layer)

---

### 2. User Mobile Application

**Path:** `/user_app`

This directory contains the **Flutter-based mobile application for end users**.

**Responsibilities:**
- User authentication
- Service discovery and booking
- Order tracking and history
- Communication with the backend API

**Target Platforms:**
- iOS
- Android

**Primary Technologies:**
- Flutter
- Dart
- REST API integration

---

### 3. Provider Mobile Application

**Path:** `/provider_app`

This directory contains the **Flutter-based mobile application for service providers** operating on the ColorCare platform.

**Responsibilities:**
- Provider authentication
- Job and service request management
- Status updates and workflow actions
- Communication with the backend API

**Target Platforms:**
- iOS
- Android

**Primary Technologies:**
- Flutter
- Dart
- REST API integration

---

## Architecture Summary

- All client applications communicate exclusively with the backend via HTTPS REST APIs.
- No direct database access is permitted from client applications.
- The backend is designed as a stateless service layer.
- Mobile and web clients share the same authentication and authorization mechanisms.

---

## Environment Separation

Each component supports multiple environments:
- Development
- Staging
- Production

Environment-specific configuration is handled through externalized configuration files and environment variables.

---

## Version Control Notes

- This repository uses a mono-repository structure.
- Each major component is logically isolated within its own directory.
- Changes affecting backend APIs must be evaluated for compatibility with both mobile applications.

---

## Document Authority

This README serves as the primary technical introduction to the ColorCare codebase.  
All contributors are expected to follow the structural conventions and architectural boundaries defined herein.

---
