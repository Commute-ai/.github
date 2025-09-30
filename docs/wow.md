# Commute.ai - Way of Working

## Repository Structure

**Organization:** [Commute-ai](https://github.com/Commute-ai)

**Code Repositories:**

- `ui` - React Native mobile app [Commute-ai/ui](https://github.com/Commute-ai/ui)
- `backend` - Python FastAPI server [Commute-ai/backend](https://github.com/Commute-ai/backend)
- `ai-agents` - AI agent implementations [Commute-ai/ai-agents](https://github.com/Commute-ai/ai-agents)
- `.github` - Organization documentation and **user stories** [Commute-ai/.github](https://github.com/Commute-ai/.github)

**GitHub Project:** Single org-level board tracking all work: [Commute-ai/projects/1](https://github.com/orgs/Commute-ai/projects/1)

## Issue Types

### User Stories (Type: `Feature`)

- High-level feature from user perspective
- Format: "As [user] I want [goal] so that [benefit]"
- Contains acceptance criteria
- Links to subtasks as checklist in description
- **Created in:** `.github` repository
- Created by: Any team member
- Example: [As a user, I want to login and see that I am logged in, so I can save my preferences](https://github.com/Commute-ai/.github/issues/5)

### Subtasks (Type: `Subtask`)

- Specific technical implementation task
- Links to parent user story
- **Created in:** The specific code repository (`ui`, `backend`, or `ai-agents`)
- Assigned to: Developer who will complete it
- Created by: Any team member
- Example: [Initialize the backend project with basic FastAPI setup](https://github.com/Commute-ai/backend/issues/1)

## Sprint Workflow

### One Week Sprints (Monday to Monday)

**Monday - Sprint Planning**

- Review last sprint completions
- Create and discuss new user stories in `.github` repo
- Break down user stories into subtasks in specific repos
- Assign subtasks to developers
- User stories tracked with weekly milestones (subtasks are not)

**During Week - Development**

- Work on assigned subtasks
- Update issue status on project board
- Create PRs when ready (or just commit to main)
- Review teammate commits or PRs
- Merge approved work

## Labels

**Type:**

- `Feature` - User story
- `Subtask` - Implementation task
- `Bug` - Fix needed
- `Docs` - Documentation
- `Chore` - Quick task not fitting above

## Branching Strategy

**Branch Structure:**

- `development` - Active development branch for next release
  - All feature work and subtasks merge here
  - Automatically deploys to **staging environment**
  - Where we develop throughout the week
  
- `main` - Production branch
  - Stable, production-ready code
  - Automatically deploys to **production environment**
  - Updated weekly after sprint completion

**Weekly Release Process:**

1. **End of Sprint (Monday):**
   - Review and test `development` branch in staging
   - Merge `development` → `main`
   - Create release tag in `main` (e.g., `v0.2.0`)
   - Production deployment triggered automatically

2. **Start of Sprint:**
   - Continue developing on `development` branch
   - New features merge to `development`

**CI/CD Pipeline:**

- Push to `development` → Auto-deploy to **staging**
- Push to `main` → Auto-deploy to **production**
- OTA updates published automatically for mobile app

## Pull Requests

- Title describes the change
- Include "Closes #N" to auto-close subtask
- **Target branch:** `development` (not `main`)
- Request review from teammate
- Merge when approved

## Weekly Subtask Board

**Columns:**

1. **Todo** - Not yet started
2. **In Progress** - Being worked on
3. **Done** - Merged and complete

## Milestones

Weekly milestones track sprint scope and **only apply to user stories** in `.github` repo: [.github/milestones](https://github.com/Commute-ai/.github/milestones)

Subtasks in code repos do not use milestones - they link to their parent user story instead.

## Communication

- **GitHub Issues:** Technical discussion, progress updates
- **Monday Meetings:** Planning, retrospectives, decisions
- **Discord:** Quick questions, daily coordination: [Commute.ai - Discord invite](https://discord.gg/75WP9k3Xum)

## Example Flow

**Monday:**

```
1. Team creates user story in .github repo: "User can login"
2. Break into subtasks in specific repos:
   - Commute-ai/backend#5 "Setup FastAPI auth" (assigned to Alice)
   - Commute-ai/ui#6 "Create login screen" (assigned to Bob)
3. Add user story to Week 1 milestone in .github
4. Link subtasks to user story in description
```

**During Week:**

```
Alice & Bob:
- Create feature branches from development
- Move issues to "In Progress" on project board
- Develop and commit code
- Create PRs targeting development branch with "Closes #5" / "Closes #6"
- Review each other's work
- Merge to development when approved
- Changes auto-deploy to staging environment
```

**End of Sprint (Next Monday):**

```
1. Test development branch in staging
2. Merge development → main
3. Create release tag (e.g., v0.2.0)
4. Auto-deploy to production
5. User story auto-completes when all subtasks done
```

---

**User stories live in `.github` repo [Commute-ai/.github](https://github.com/Commute-ai/.github). Subtasks live in their specific code repositories (`ui`, `backend`, `ai-agents`).**
