# Commute.ai - Way of Working

## Repository Structure

**Organization:** [Commute-ai](https://github.com/Commute-ai)

**Code Repositories:**

- `ui` - React Native mobile app [Commute-ai/ui](https://github.com/Commute-ai/ui)
- `backend` - Python FastAPI server [Commute-ai/backend](https://github.com/Commute-ai/backend)
- `ai-agents` - AI agent implementations [Commute-ai/ai-agents](https://github.com/Commute-ai/ai-agents)
- `commute.ai` - Documentation and **all issues/project management** [Commute-ai/commute.ai](https://github.com/Commute-ai/commute.ai)

**GitHub Project:** Single org-level board tracking all work: [Commute-ai/projects/1](https://github.com/orgs/Commute-ai/projects/1)

## Issue Types

### User Stories (Type: `Feature`)

- High-level feature from user perspective
- Format: "As [user] I want [goal] so that [benefit]"
- Contains acceptance criteria
- Links to subtasks as checklist in description
- Created by: Any team member
- Example: [As a user, I want to login and see that I am logged in, so I can save my preferences](https://github.com/Commute-ai/commute.ai/issues/5)

### Subtasks (Type: `Subtask`)

- Specific technical implementation task
- Links to parent
- Assigned to: Developer who will complete it
- Created by: Any team member
- Example: [Initialize the backend project with basic FastAPI setup](https://github.com/Commute-ai/commute.ai/issues/12)

## Sprint Workflow

### One Week Sprints (Monday to Monday)

**Monday - Sprint Planning**

- Review last sprint completions
- Create and discuss new user stories
- Break down user stories into subtasks
- Assign subtasks to developers?
- Add everything to weekly milestone

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
- `Chore` - Some quick task not fitting above

**Component:**

- `ui` - React Native work
- `backend` - FastAPI work
- `ai-agents` - AI work
- `infra` - DevOps/tooling

## Pull Requests

- Title describes the change
- Include "Closes #N" to auto-close subtask
- Request review from teammate
- Merge when approved
- Developer decides on branching strategy

## Weekly Subtask Board

**Columns:**

1. **Todo** - Not yet started
2. **In Progress** - Being worked on
3. **Done** - Merged and complete

## Milestones

Weekly milestones track sprint scope: [commute.ai/milestones](https://github.com/Commute-ai/commute.ai/milestones)

## Communication

- **GitHub Issues:** Technical discussion, progress updates
- **Monday Meetings:** Planning, retrospectives, decisions
- **Discord:** Quick questions, daily coordination: [Commute.ai - Discord invite](https://discord.gg/75WP9k3Xum)

## Example Flow

**Monday:**

```
1. Team creates user story: "User can login"
2. Break into subtasks:
   - #5 "Setup FastAPI auth" (backend, assigned to Alice)
   - #6 "Create login screen" (ui, assigned to Bob)
3. Add to Week 1 milestone
```

**During Week:**

```
Alice & Bob:
- Move issues to "In Progress"
- Develop and commit code
- Create PRs with "Closes #5" / "Closes #6"
- Review each other's work
- Merge when approved
- User story auto-completes when all subtasks done
```

---

**All issues live in `commute.ai` repo [Commute-ai/commute.ai](https://github.com/Commute-ai/commute.ai). Use component labels to indicate which codebase they affect.**
