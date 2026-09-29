# FitFlow High-Level Architecture

## Architecture Overview

FitFlow follows a layered and service-oriented architecture.

The Flutter frontend communicates with the main backend through APIs. Firebase Authentication manages user identity. The NestJS backend coordinates PostgreSQL, Redis, WebSockets, and the FastAPI AI microservice.

## Main Components

| Component | Technology / Purpose |
|---|---|
| Frontend | Flutter (Dart) – Android, iOS and web interface |
| Backend | Node.js + NestJS – APIs, business logic and service coordination |
| AI Microservice | Python + FastAPI – workout recommendations and AI processing |
| Database | PostgreSQL – user, workout, nutrition, progress and community data |
| Authentication | Firebase Authentication – identity and login management |
| Cache | Redis – frequently accessed data and response optimization |
| Real-Time Layer | WebSockets – live community updates and notifications |

## Critical Data Flow 1 – Personalized Workout Plan

User → Flutter Frontend → NestJS Backend → FastAPI AI Service → Personalized Workout Plan → NestJS → PostgreSQL → Flutter Frontend

The user provides fitness goals, preferences, schedule, and relevant information through Flutter. NestJS validates and forwards the required information to the AI service. FastAPI generates a personalized plan and returns it to NestJS. The plan is stored in PostgreSQL and displayed to the user.

## Critical Data Flow 2 – Social Sharing

User → Flutter Frontend → NestJS Backend → PostgreSQL → WebSocket Layer → Other Connected Users

When a user shares a workout achievement or interacts with a community feature, NestJS processes the request and stores the relevant information. WebSockets then distribute appropriate live updates to connected users. Authentication and authorization controls are applied before protected actions are accepted.

## Critical Data Flow 3 – Nutrition Tracking

User → Flutter Frontend → NestJS Backend → AI Service → Nutrition Result → PostgreSQL → Flutter Frontend

The user records a meal through the nutrition interface. The backend can call the AI service when food recognition or recommendation processing is required. The resulting nutrition information is stored in PostgreSQL and presented through the application.

## Security

- Firebase Authentication provides identity management.
- HTTPS should protect communication between client and services.
- Backend APIs should validate inputs and authorize protected operations.
- Sensitive application data should be protected through appropriate database access controls.
- Health-related information should be handled according to applicable privacy and security requirements.

## Scalability

- NestJS provides a structured backend that can be scaled as traffic grows.
- Redis can reduce repeated database reads.
- The AI service can be scaled independently from the main backend.
- PostgreSQL can support increasing structured application data with appropriate indexing and deployment configuration.
- WebSocket infrastructure can be scaled as community usage increases.

## Integration

- Flutter communicates with NestJS through APIs.
- NestJS communicates with FastAPI for AI operations.
- PostgreSQL stores core application data.
- WebSockets deliver real-time community events.
- Firebase Authentication provides authentication independently of the application database.
