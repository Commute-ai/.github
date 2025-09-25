# Commute.ai - Architecture (WIP)

## Components

### Mobile App (`ui`)
- React Native/Flutter frontend
- Route input and preference settings
- Displays AI-enhanced route recommendations

### Backend API (`backend`)
- Python FastAPI + SQLAlchemy + PostgreSQL
- HSL API integration and route orchestration
- User management and preferences storage
- Passes HSL route data to AI agents
- Returns enhanced routes to mobile app

### AI Agents API (`ai-agents`)
- OpenAI/HuggingFace integration + own database
- Receives route context from backend
- Fetches and processes social media data
- Returns route insights and scoring to backend

## Data Flow (WIP)

1. Mobile app sends route request to backend
2. Backend fetches HSL routes and user preferences
3. Backend sends route context to AI agents
4. AI agents fetch social media data and process insights
5. AI agents return enhanced route scoring to backend
6. Backend returns personalized routes to mobile app

## Database Strategy

**Backend Database:**
- Users, preferences, saved routes
- HSL route cache
- Authentication data

**AI Agents Database:**
- Social media insights cache (12-24h TTL)
- Route sentiment scores?
- User preference learning patterns?

## Social Media Data Handling

**Cached (with TTL):**
- Processed route insights
- Community sentiment scores
- Construction/disruption reports

**Real-time Fetch:**
- Breaking transit alerts
- Weather-dependent insights
- Fresh social media posts (jodel) ?

## External Integrations

- HSL API (Helsinki transit data)
- Social media APIs (Reddit, Jodel, local forums)
- Weather services
- OpenAI/AI model APIs

## Deployment

**Hosting:** Coolify self-hosted platform on DigitalOcean droplet

Dashboard available here: [coolify.commute.ai.ender.fi](https://coolify.commute.ai.ender.fi/)

**CI/CD Pipeline:**
- Push to `main` branch triggers GitHub webhook
- Coolify auto-builds Docker containers
- Automatic deployment with health checks
- Zero-downtime rolling updates
