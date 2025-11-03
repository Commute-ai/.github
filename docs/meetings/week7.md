# Commute.ai - Planning week 7 (2025-11-03)

## What needs to be done

- [x] Fill the development diary
    - Viljami will do it
- [ ] The insight endpoint (Zijad)
- [ ] What is the status?
- [ ] Demo in one week. What is needed?
- [ ] The app should be working
- [ ] User stories for week 7

## Notes

- insight/itineraries endpoints
    - No need to send back the itineraries and legs from ai-agents to backend
        - Viljami will create a task to only return insights in the same order from the ai-agents
        - Always return the insights in the same order as the backend sends them
    - Update the requestschema in backend to reflect ai-agents
    - Update the backend to call `/insight/itineraries` instead of `/insight/routes`

- How to contact the LLM Api with ResponseFormat
