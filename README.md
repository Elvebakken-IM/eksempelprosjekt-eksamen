# 📦 README.md – Node.js Shopping Platform

## 🧭 Overview

This project is a full-stack **e-commerce web application** built with:

* Node.js (backend runtime)
* Express.js (web framework)
* MongoDB + Mongoose (database)
* EJS (templating engine)
* Stripe (payments)
* PDFKit (invoice generation)

The application supports a full shopping flow:

* Authentication (signup/login/reset password)
* Product management (CRUD)
* Shopping cart
* Orders & payments
* Invoice generation ([GitHub][1])

---

## 🖼️ System Overview (Architecture)

```mermaid
flowchart LR
    User[👤 User Browser]
    Frontend[EJS Views]
    Backend[Node.js + Express]
    DB[(MongoDB)]
    Stripe[(Stripe API)]

    User --> Frontend
    Frontend --> Backend
    Backend --> DB
    Backend --> Stripe
    Stripe --> Backend
    Backend --> Frontend
```

---

## 🧱 Application Architecture (Layered)

```mermaid
flowchart TB
    subgraph Presentation Layer
        Views[EJS Templates]
    end

    subgraph Application Layer
        Controllers[Controllers]
        Routes[Routes]
        Middleware[Middleware]
    end

    subgraph Domain Layer
        Services[Business Logic]
        Models[Mongoose Models]
    end

    subgraph Infrastructure
        DB[(MongoDB)]
        External[Stripe / Email / PDF]
    end

    Views --> Controllers
    Controllers --> Services
    Services --> Models
    Models --> DB

    Services --> External
```

---

## 🗂️ Project Structure

```
.
├── controllers/
├── middleware/
├── models/
├── routes/
├── views/
├── public/
├── utils/
├── app.js
├── package.json
```

💡 Dette er en klassisk MVC-struktur:

* **Models** → database
* **Views** → UI
* **Controllers** → logikk

---

## 🧬 Data Model (MongoDB / Mongoose)

```mermaid
erDiagram
    USER {
        string _id
        string email
        string password
        array cart
    }

    PRODUCT {
        string _id
        string title
        number price
        string description
        string imageUrl
        string userId
    }

    ORDER {
        string _id
        object user
        array products
    }

    CART_ITEM {
        string productId
        number quantity
    }

    USER ||--o{ CART_ITEM : has
    PRODUCT ||--o{ CART_ITEM : referenced_in
    USER ||--o{ ORDER : places
    ORDER ||--o{ PRODUCT : contains
```

---

## 🔄 Key Flows

### 🛒 Add to Cart

```mermaid
sequenceDiagram
    participant U as User
    participant FE as Frontend
    participant BE as Backend
    participant DB as Database

    U->>FE: Click "Add to cart"
    FE->>BE: POST /cart
    BE->>DB: Update user.cart
    DB-->>BE: OK
    BE-->>FE: Updated cart
```

---

### 💳 Checkout Flow (Stripe)

```mermaid
sequenceDiagram
    participant U as User
    participant BE as Backend
    participant Stripe as Stripe API

    U->>BE: Checkout request
    BE->>Stripe: Create payment
    Stripe-->>BE: Payment session
    BE-->>U: Redirect to Stripe
    Stripe-->>BE: Payment success webhook
    BE->>BE: Create order
```

---

## ⚙️ Tech Stack (Tech Docs)

### Backend

| Technology | Purpose     |
| ---------- | ----------- |
| Node.js    | Runtime     |
| Express    | HTTP server |
| Mongoose   | ORM         |
| MongoDB    | Database    |

---

### Frontend

| Technology | Purpose               |
| ---------- | --------------------- |
| EJS        | Server-side rendering |
| CSS        | Styling               |

---

### Integrations

| Service | Purpose            |
| ------- | ------------------ |
| Stripe  | Payments           |
| PDFKit  | Invoice generation |

---

## 🔐 Security Considerations

* Password hashing (bcrypt)
* CSRF protection
* Input validation
* Secure session handling

---

## 🚀 Getting Started

```bash
git clone https://github.com/gaetanBloch/nodejs-shopping
cd nodejs-shopping
npm install
npm start
```

Open:

```
http://localhost:3000
```

---

## 🧠 Design Decisions

### Why Node.js?

* Non-blocking I/O → good for many concurrent users
* Event-driven architecture → scalable e-commerce backend

### Why MongoDB?

* Flexible schema → easy product modeling
* Good fit with JSON-based APIs

---

## 📈 Possible Improvements

### Architecture

* Split into microservices
* Introduce API layer (REST / GraphQL)

### Performance

* Redis caching (cart/session) ([Redis][2])
* CDN for images

### DevOps

* Dockerize app
* CI/CD pipeline

---

## 🧪 Testing Strategy

* Unit tests (controllers/services)
* Integration tests (API routes)
* End-to-end tests (checkout flow)

---

## 🧭 Roadmap

* [ ] Admin dashboard (analytics)
* [ ] Product search & filtering
* [ ] Wishlist feature
* [ ] Multi-tenant support
