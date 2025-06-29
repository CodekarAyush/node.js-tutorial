# 🚀 Node.js Backend Development Notes

This repository contains topic-wise structured notes and code samples to build a **highly scalable Node.js backend system**, starting from core fundamentals to advanced architecture and tooling.

---

## 🧭 Index

### 🟢 1. Node.js Core Concepts
- [1.1 How Node.js Works – Event Loop, Single Threaded Non-blocking I/O](./01-core/how-nodejs-works.md)
- [1.2 Node.js Built-in Modules](./01-core/built-in-modules.md)
  - `fs`, `path`, `http`, `url`, `os`, `crypto`, etc.
- [1.3 Events and EventEmitter](./01-core/event-emitter.md)
- [1.4 Streams – Readable, Writable, Duplex, Transform](./01-core/streams.md)
- [1.5 Buffer & Encoding](./01-core/buffer.md)
- [1.6 Cluster Module – Load Balancing](./01-core/cluster.md)
- [1.7 Worker Threads – Parallelism in Node.js](./01-core/worker-threads.md)
- [1.8 Child Processes – `exec`, `spawn`, `fork`](./01-core/child-process.md)

---

### 🧰 2. Node.js Project Essentials
- [2.1 npm, package.json, scripts](./02-essentials/npm-package.md)
- [2.2 Environment Variables & `.env` Handling](./02-essentials/env-config.md)
- [2.3 Debugging & Logging](./02-essentials/logging-debugging.md)
- [2.4 File Upload & Compression (zlib, archiver)](./02-essentials/file-compression.md)
- [2.5 Rate Limiting, Helmet & CORS](./02-essentials/security.md)

---

### ⚙️ 3. Express.js Fundamentals
- [3.1 Express Setup & Routing](./03-express/routing.md)
- [3.2 Middleware & Error Handling](./03-express/middleware.md)
- [3.3 Async Controllers with `express-async-handler`](./03-express/async-controller.md)
- [3.4 Request Validation using `vine.js`](./03-express/vine-validation.md)
- [3.5 File Uploads using `multer`](./03-express/file-upload.md)
- [3.6 Authentication with JWT](./03-express/auth-jwt.md)
- [3.7 Role-Based Access Control](./03-express/rbac.md)

---

### 🧱 4. Database Layer
- [4.1 PostgreSQL & Prisma ORM Basics](./04-database/prisma-setup.md)
- [4.2 Relations, Filters, Pagination with Prisma](./04-database/prisma-relations-pagination.md)
- [4.3 Prisma Middleware & Transactions](./04-database/prisma-advanced.md)
- [4.4 Prisma + Express Integration](./04-database/prisma-express.md)

---

### 🧪 5. Testing & Debugging
- [5.1 Unit Testing with Jest](./05-testing/jest.md)
- [5.2 Supertest for API Testing](./05-testing/supertest.md)
- [5.3 Mocking & Coverage](./05-testing/mocking.md)

---

### 📦 6. Redis, Queues, and Kafka
- [6.1 Caching with Redis](./06-scaling/redis.md)
- [6.2 Pub/Sub using Redis](./06-scaling/redis-pubsub.md)
- [6.3 Background Jobs with BullMQ](./06-scaling/bullmq.md)
- [6.4 Kafka Basics & Integration](./06-scaling/kafka.md)

---

### 🔌 7. Real-time & Streaming
- [7.1 WebSockets vs Socket.IO](./07-realtime/socketio.md)
- [7.2 Socket.IO Chat Example](./07-realtime/chat-app.md)
- [7.3 HLS Streaming & Bitrate Handling](./07-realtime/hls-streaming.md)

---

### 🪝 8. Webhooks & External APIs
- [8.1 Creating & Consuming Webhooks](./08-webhooks/webhook-basics.md)
- [8.2 Stripe Webhooks Example](./08-webhooks/stripe.md)

---

### 🧱 9. TypeScript Setup for Backend
- [9.1 TSConfig Setup](./09-typescript/tsconfig.md)
- [9.2 Express + TypeScript](./09-typescript/express-ts.md)
- [9.3 Type-Safe Controllers & DTOs](./09-typescript/controllers-dtos.md)

---

### 🧠 10. Design Patterns & Architecture
- [10.1 Folder Structure Best Practices](./10-architecture/structure.md)
- [10.2 Service Layer & Repository Pattern](./10-architecture/repository-pattern.md)
- [10.3 Clean Architecture](./10-architecture/clean-arch.md)

---

### 🧱 11. NestJS (Advanced Backend Framework)
- [11.1 NestJS Introduction](./11-nestjs/nest-intro.md)
- [11.2 Controllers, Modules, Providers](./11-nestjs/basics.md)
- [11.3 Dependency Injection](./11-nestjs/di.md)
- [11.4 Validation with Class Validator](./11-nestjs/validation.md)
- [11.5 TypeORM Integration](./11-nestjs/typeorm.md)
- [11.6 Auth, Guards, Interceptors](./11-nestjs/auth-guards.md)
- [11.7 Microservices with Kafka & Redis](./11-nestjs/microservices.md)

---

### 🚀 12. Deployment & DevOps
- [12.1 PM2 Process Manager](./12-deployment/pm2.md)
- [12.2 Dockerize Node.js App](./12-deployment/docker.md)
- [12.3 CI/CD with GitHub Actions](./12-deployment/github-actions.md)
- [12.4 Environment Promotion Strategy (Dev/Staging/Prod)](./12-deployment/env-strategy.md)

---

## 🔗 Useful References
- [Node.js Docs](https://nodejs.org/en/docs)
- [Prisma Docs](https://www.prisma.io/docs)
- [NestJS Docs](https://docs.nestjs.com)
- [Redis Official Site](https://redis.io/)
- [Kafka Documentation](https://kafka.apache.org/documentation/)

---

## 📌 Note
This repo is a work in progress. Feel free to fork, clone, and contribute!

---

