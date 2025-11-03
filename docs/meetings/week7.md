# Commute.ai - Planning week 7 (2025-11-03)

## What needs to be done

- [x] Fill the development diary
  - Viljami will do it
- [x] The insight endpoint (Zijad)
- [x] What is the status?
    - ai-agents is lagging behind backend, ui
    - we are confident of getting the demo #2 features done in time
- [x] Demo in one week. What is needed?
    - Have a short demo about the app
    - Talk about what we will prepare for the final demo
    - Meet on monday at around 15:00 before the lecture
- [x] Next weeks meeting
    - Tuesday at 17:00
- [x] The app should be working
    - Viljami will double check the app 
- [x] User stories for week 7

## Notes

- insight/itineraries endpoint
  - No need to send back the itineraries and legs from ai-agents to backend
    - Viljami will create a task to only return insights in the same order from the ai-agents
    - Always return the insights in the same order as the backend sends them
  - Update the requestschema in backend to reflect ai-agents
  - Update the backend to call `/insight/itineraries` instead of `/insight/routes`
- Decided that we will take multiple iteneraries instead of one
- How to contact the LLM Api with ResponseFormat
    - Update the agent implementation according to Antti's pull request
```python
response_format=cast(ResponseFormatJSONSchema, {
  'type': "json_schema",
  'json_schema': {
  "name": 'OutputSchema',
  "schema": Output.model_json_schema()
  }),
```
