# ADR-001: Selection of FitFlow Technology Architecture

## Status

Accepted

## Context

FitFlow requires Android, iOS and web support, AI-powered personalization, nutrition tracking, social features, real-time updates, secure authentication, and scalable structured data management.

## Decision

Use Flutter for the frontend, Node.js/NestJS for the main backend, Python/FastAPI for the AI microservice, PostgreSQL for the main database, Firebase Authentication for identity, Redis for caching, and WebSockets for real-time communication.

## Rationale

The architecture combines cross-platform development, maintainable backend structure, a strong AI ecosystem, relational data consistency, straightforward authentication, caching, and real-time communication.

## Consequences

The architecture provides separation of responsibilities and independent scaling of AI processing, but it introduces multiple services that require configuration, monitoring, security controls, and team knowledge across several technologies.
