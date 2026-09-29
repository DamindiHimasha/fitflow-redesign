# FitFlow Redesign

## Project Description

FitFlow is a fitness application redesign that provides a seamless experience across Android, iOS, and web platforms. The system supports personalized workout planning, nutrition tracking, progress monitoring, and social community features.

## Objectives

The main objectives of the FitFlow redesign are:

- Provide a cross-platform fitness application.
- Support personalized workout recommendations.
- Support nutrition tracking.
- Provide progress tracking.
- Provide social and real-time community features.
- Maintain secure user authentication.
- Provide a scalable and maintainable system architecture.

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | Flutter (Dart) |
| Main Backend | Node.js + NestJS |
| AI Microservice | Python + FastAPI |
| Database | PostgreSQL |
| Authentication | Firebase Authentication |
| Caching | Redis |
| Real-Time Layer | WebSockets |

## Main Features

- User authentication
- Personalized workout plans
- Workout management
- Nutrition tracking
- Progress tracking
- Social community features
- Real-time updates
- AI-powered recommendations

## System Architecture

FitFlow uses a layered and service-oriented architecture.

The Flutter frontend communicates with the Node.js/NestJS backend through APIs. Firebase Authentication manages user identity. NestJS coordinates PostgreSQL, Redis, WebSockets, and the FastAPI AI microservice.

### Architecture Diagram

The high-level architecture diagram is available in:

`docs/architecture-diagram.png`

## Repository Structure

```text
fitflow-redesign/
│
├── frontend/
├── backend/
├── ai-service/
├── docs/
│   ├── technology-comparison.md
│   ├── decision-matrix.md
│   ├── architecture.md
│   ├── architecture-diagram.png
│   └── ADR.md
├── README.md
└── .gitignore
