# Commute.ai kickoff (2024-09-22)

## What needs to be done

- [x] Return the kawasaki presentation in moodle.
  - Zijad
- [x] Register the group in moodle.
- [x] Return a diary of the first week in moodle.
  - Antti
- [x] Init a github repository for the project.
  - Multi-repo
- [x] Go thru the schedule and milestones.
- [x] Meetings
  - Every week on monday
  - Communication on discord
- [x] Plan the architecture roughly.
- [x] Create user stories for the first milestone.
- [x] Decide the time of the next session.

## Architecture planning

- Go thru the vision
  - What do we want to achieve?
  - What are the main features?
  - What do we want the MVP to be?
  - What are things we want to focus on?

  - A HSL-like mobile app where user can choose points A and B, then the app suggests routes from HSL, then enhances the routes with data from AI agents.
  - Users can input realtime data on routes or lines and our app will store that data globally
    - Monitor trends like how full lines are on specific times

- High level components
  - UI (mobile app)
  - Backend (API, database)
    - integrates with HSL api
    - integrates with some database?
    - integrates with AI agents
  - AI agents (preference agent, social agent, recommendation agents...)
    - integrates with OpenAI or other LLMs

- AI agent architecture
  - Preference agent, social agent, recommendation agents
  - How do we want to structure the agents?
  - What kind of agents do we want?
  - How do we want to handle communication between agents?
- Technical stack
  - Frontend: React, Vue, Svelte?
  - Backend: Node.js, Python, Go?
  - Database: PostgreSQL, MongoDB, Firebase?
  - AI: OpenAI, HuggingFace, custom models?
- Team structure and responsibilities
  - Who will be responsible for what?
  - How will we handle collaboration and communication?
