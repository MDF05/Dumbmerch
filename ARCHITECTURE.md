# System Architecture

This document describes the high-level architecture of the **dumbmerch** platform. It outlines the system boundaries, technology choices, and communication patterns between its components.

## 🏗 High-Level Overview

**dumbmerch** follows a classic **client-server** architecture using a decoupled frontend and backend. 

- **Frontend**: A Single Page Application (SPA) built with React and Vite, responsible for the user interface and client-side logic.
- **Backend**: A RESTful API built with Node.js and Express, responsible for business logic, data persistence, and third-party integrations.
- **Database**: Relational database (PostgreSQL) managed via Prisma ORM.

## 🧩 Component Diagram

```mermaid
graph TD
    subgraph Client [Frontend Layer]
        Browser[Web Browser]
        ReactApp[React SPA (Vite)]
    end

    subgraph Server [Backend Layer]
        API[Express API Gateway]
        Auth[Auth Service (JWT)]
        BizLogic[Business Logic]
        Socket[Socket.io / WS Server]
    end

    subgraph Data [Data Layer]
        DB[(PostgreSQL Database)]
        Prisma[Prisma ORM]
    end

    subgraph External [External Services]
        Cloudinary[Cloudinary (Images)]
        Midtrans[Midtrans (Payment)]
        SMTP[SMTP / Nodemailer]
    end

    %% Connections
    Browser -- HTTP/HTTPS --> ReactApp
    ReactApp -- REST API (Axios) --> API
    ReactApp -- WebSocket --> Socket
    
    API --> Auth
    API --> BizLogic
    BizLogic --> Prisma
    Prisma --> DB

    %% External Integrations
    BizLogic -- Uploads --> Cloudinary
    BizLogic -- Transactions --> Midtrans
    BizLogic -- Emails --> SMTP
```

## 🔌 Communication Patterns

### Client-Server
- **Protocol**: HTTP/1.1 (REST)
- **Real-time**: WebSocket (Socket.io) for live notifications or updates.
- **Data Exchange**: JSON format.

### Internal Layers (Backend)
- **Controller-Service-Repository**: The backend likely follows a modular pattern where Controllers handle HTTP requests, Services contain business logic, and Repositories (via Prisma) handle DB access.

## 🛠 Technology Stack Validation

### Frontend
| Technology | Usage | Justification |
| :--- | :--- | :--- |
| **React** | UI Framework | Component-based, declarative UI. |
| **Vite** | Build Tool | Extremely fast HMR and build times. |
| **TypeScript** | Language | Static typing for reliability. |
| **Chakra UI / Tailwind** | Styling | Rapid UI development and consistent design system. |
| **Redux Toolkit** | State Management | Predictable state container for complex flows. |

### Backend
| Technology | Usage | Justification |
| :--- | :--- | :--- |
| **Node.js & Express** | Server | Event-driven, non-blocking I/O for high throughput. |
| **TypeScript** | Language | Type safety sharing with Frontend. |
| **Prisma** | ORM | Type-safe database queries and schema management. |
| **PostgreSQL** | Database | ACID compliant, robust relational database. |
| **Zod** | Validation | Runtime schema validation. |

## 📦 Service Boundaries

| Service | Responsibility |
| :--- | :--- |
| **User Service** | Registration, Login, Profile Management (JWT based). |
| **Product Service** | CRUD operations for merchandise items. |
| **Order Service** | Checkout flow, order tracking. |
| **Payment Service** | Interface with Midtrans for processing payments. |
| **Media Service** | Handling file uploads to Cloudinary. |

## 🔄 Deployment Architecture (Proposed)

Ideally, this monorepo can be deployed as follows:
- **Frontend**: Static hosting (Vercel, Netlify, or S3+CloudFront).
- **Backend**: Containerized (Docker) and deployed to a cloud provider (AWS ECS, DigitalOcean App Platform, or Heroku), or a VPS (EC2).
- **Database**: Managed PostgreSQL instance (AWS RDS, Supabase, or Neon).
