# Activity 2: Compare Backend, Database and Authentication Options

## Backend Frameworks

| Criteria | Node.js / NestJS | Python / FastAPI | Go |
|----------|-------------------|-------------------|-----|
| Dev speed | Fast, TypeScript, large ecosystem | Fast, concise, great for APIs | Moderate — more boilerplate |
| AI/ML integration | Possible via services | Excellent — native Python ML stack | Weak — limited ML libraries |
| Real-time capability | Excellent (WebSockets, Socket.io) | Good (WebSockets supported) | Excellent (goroutines) |
| Maintainability (mid team) | High — structured, TypeScript | High — typed, simple structure | Medium — smaller talent pool |
| Security | Strong — mature middleware | Strong — built-in validation | Strong — compiled, safe |

## Database Options

| Criteria | PostgreSQL | MongoDB | Firebase (Firestore) | DynamoDB |
|----------|-----------|---------|------------------------|-----------|
| Scalability | Vertical + read replicas | Horizontal, flexible | Auto-scales (managed) | Auto-scales (managed) |
| Query performance | Excellent for relational/joins | Good for document queries | Good for simple real-time reads | Fast key-value lookups only |
| Health data handling | Strong — structured, ACID-compliant | Moderate — schema-less risk | Weak for structured health records | Weak for relational health data |
| Cost (mid-size team) | Low (self-host or managed) | Low–medium | Low to start, scales with usage | Pay-per-request, can add up |

## Authentication Options

| Criteria | Firebase Auth | AWS Cognito | Auth0 | Supabase Auth |
|----------|---------------|-------------|-------|-----------------|
| Security / compliance | Good, GDPR-capable | Strong, HIPAA-eligible on AWS | Strong, enterprise compliance add-ons | Good, GDPR-capable |
| Integration ease | Very easy (esp. with Firebase) | Moderate — more config | Easy, well-documented | Easy (pairs with Postgres) |
| Cost (mid team) | Free tier generous | Free tier, scales with MAUs | Costs rise quickly at scale | Free tier generous |
| Real-time synergy | Excellent (same ecosystem) | Neutral | Neutral | Good (pairs with Postgres realtime) |

## Recommendation

Use Node.js/NestJS as the main API because it works well with Flutter and handles real-time features nicely. Add a Python/FastAPI microservice just for AI/ML work. Use PostgreSQL as the main database because it is safe and structured for health data. Add Firebase Firestore for real-time social feeds and notifications. Use Firebase Auth for login because it is cheap, easy to set up, and works well with Firestore.
