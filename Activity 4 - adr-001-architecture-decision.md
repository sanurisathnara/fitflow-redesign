# Activity 4: High-Level Architecture

## Architecture Decision Record (ADR-001)

| Field | Detail |
|-------|--------|
| Title | Adopt Flutter + Node.js/NestJS + FastAPI + PostgreSQL + Firebase for FitFlow redesign |
| Status | Accepted |
| Context | FitFlow needs one codebase across iOS/Android/web, fast AI feature delivery, real-time social features, and compliant handling of health data, built by a mid-sized team on a tight timeline. |
| Decision | Use Flutter for all client apps; Node.js/NestJS as the core API; a separate Python/FastAPI microservice for AI/ML; PostgreSQL for structured/compliance-sensitive data; Firebase (Firestore, Auth, Cloud Messaging, Storage) for real-time and identity features; Redis for caching and session/rate-limit data. |
| Consequences | + Fastest path to a unified iOS/Android/web app with strong AI support and low cost.<br>− Team must manage two backend runtimes (Node.js and Python) instead of one.<br>− Splitting data between PostgreSQL and Firestore requires clear ownership rules per data type to avoid duplication or drift. |
