# 📚 Digital Library — Backend

A **Spring Boot–based Digital Library Management System** that integrates **GitHub OAuth2 login**, **Redis caching**, and **PostgreSQL persistence**.  
Built following clean architecture and layered design principles — developed as part of an advanced backend engineering course.

---
## 🚀 Features

- 🔐 **OAuth2 GitHub Login** — secure authentication with GitHub
- 📖 **Book Management** — add, update, delete, and fetch book details
- 👥 **User Management** — manage users and their roles (admin, member)
- 💳 **Membership Handling** — assign and monitor library memberships
- ⚡ **Redis Caching** — optimize performance for frequently accessed data
- 🧩 **Aspect-Oriented Logging (AOP)** — clean logging through cross-cutting concerns
- 🧱 **Layered Architecture** — controllers → services → repositories → database
- 🧰 **Validation, Exception Handling, and DTO Mapping** included

---

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-------------|
| **Language** | Java 17 |
| **Framework** | Spring Boot 3.4.4 |
| **Security** | Spring Security + OAuth2 Client (GitHub) |
| **Database** | PostgreSQL |
| **Caching** | Redis |
| **ORM** | Spring Data JPA |
| **Logging & AOP** | AspectJ |
| **Build Tool** | Maven |
| **Testing** | JUnit 5, Spring Boot Test |
| **Utilities** | Lombok, Validation API |

---

## 🧰 API Overview
- Method	Endpoint	Description
- GET	/api/books	Fetch all books
- POST	/api/books	Add a new book
- GET	/api/users	Get user list
- POST	/api/membership	Add membership
- GET	/api/library/status	Check library service health

--- 

## 📦 Project Highlights
- Clean separation between input/output entities, domain models, and database entities

- Integrated GitHub OAuth2 for modern authentication

- Uses RedisService for caching frequently accessed queries

- Implements LoggingAspect with AspectJ for uniform logging

- Well-structured exception handling (MembershipException, ResourceNotFoundException, etc.)

---

## 🧱 Folder Summary
- Folder	Description
- /controller	Exposes REST APIs
- /service	Business logic layer
- /repository	JPA repositories for PostgreSQL
- /entities	DTOs for API requests/responses
- /configurations	Security & Redis configuration
- /mappers	Converts between DTOs and Models
- /enums	Enum definitions for roles and plans
- /beans	AOP logging and shared components