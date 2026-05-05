# Online Makeup Course Platform

A web application for purchasing and watching makeup courses, built as a university project for the **Internet Technologies 2025** course at the Faculty of Organizational Sciences, University of Belgrade.

> Forked from [elab-development/internet-tehnologije-2025-appkupovinakursevazasminkanje_2022_0117](https://github.com/elab-development/internet-tehnologije-2025-appkupovinakursevazasminkanje_2022_0117)

---

## About the Project

This platform enables users to browse, purchase, and watch makeup courses online. It supports three user roles — clients, educators, and administrators — each with a dedicated set of features. The goal is to provide a seamless and accessible experience for learning makeup techniques, independent of location or time, while also offering educators a space to digitize and sell their knowledge.

---

## Features

### For Clients
- Register and create a personal account
- Log in securely
- Browse available courses: makeup, permanent eyebrow and lip makeup
- Purchase courses and pay online via Stripe
- Watch video lessons within the application
- View purchased courses and track learning progress

### For Educators
- Add, edit, and delete courses
- Upload video lessons, descriptions, prices, and additional materials
- View course sales data and client information

### For Administrators
- Monthly reports on client activity
- Course sales statistics
- Manage clients and educators
- Add new users to the platform

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js + React + Tailwind CSS |
| Backend | Next.js API Routes |
| Database | PostgreSQL (via Drizzle ORM) |
| Authentication | NextAuth.js |
| Payments | Stripe |
| Media Storage | Cloudinary |
| Containerization | Docker + Docker Compose |

---

## Project Structure

```
/
├── src/                  # Application code (components, pages, API routes)
├── public/               # Static assets (images, icons)
├── drizzle.config.ts     # Database configuration
├── Dockerfile            # Multi-stage build for Next.js
└── docker-compose.yml    # Service definitions: web, db, stripe
```

---

## Git Branch Strategy

The project follows a structured Git branching strategy that allows parallel development across features.

| Branch | Purpose |
|---|---|
| `main` | Stable, production-ready version of the project |
| `develop` | Integration branch — feature branches merge here before `main` |
| `feature/docker` | Docker support: Dockerfile, .dockerignore, docker-compose.yml |
| `feature/tests` | Automated tests for backend and frontend, run via CI/CD pipeline |

---

## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/) and Docker Compose
- A Stripe account for payment processing
- A Cloudinary account for media uploads

### Installation

**1. Clone the repository:**

```bash
git clone https://github.com/tijanam13/internet-tehnologije-2025-appkupovinakursevazasminkanje_2022_0117.git
cd internet-tehnologije-2025-appkupovinakursevazasminkanje_2022_0117
```

**2. Create a `.env` file with the required variables:**

```env
DATABASE_URL=postgres://user:password@db:5432/database
NODE_ENV=production
JWT_SECRET=your_jwt_secret
NEXTAUTH_SECRET=your_nextauth_secret
NEXTAUTH_URL=http://localhost:3000
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=your_cloud_name
NEXT_PUBLIC_CLOUDINARY_UPLOAD_PRESET=your_upload_preset
NEXT_PUBLIC_APP_URL=http://localhost:3000
NEXT_PUBLIC_BASE_URL=http://localhost:3000/api
STRIPE_SECRET_KEY=your_stripe_key
```

**3. Start the application with Docker:**

```bash
docker-compose up --build
```

The app will be available at `http://localhost:3000`.

---

## Team

Built for the **Internet Technologies 2025** course at the Faculty of Organizational Sciences, University of Belgrade, by:

- [@andrijanaopacic](https://github.com/andrijanaopacic)
- [@tijanam13](https://github.com/tijanam13)
- [@andjelaaNikolic](https://github.com/andjelaaNikolic)

---

## License

This project was created for educational purposes as part of a university course assignment at the Faculty of Organizational Sciences, University of Belgrade.
