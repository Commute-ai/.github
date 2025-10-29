# Commute.ai Terminology Reference

## Core Domain Concepts

| Term               | Definition                                                                                 | Example                                                     |
| ------------------ | ------------------------------------------------------------------------------------------ | ----------------------------------------------------------- |
| **Itinerary**      | A combination of different transportation modes at certain times to reach from origin to destination.
For example, walking to a bus stop, taking a bus for two stops and then walking to the final destination.
Commonly used synonym: journey    | 45-min journey: walk 5 min → bus 35 min → walk 5 min        |
| **Leg**            | One part of an itinerary, e.g. walking to a bus stop or a bus ride between two stops.                                 | Walking to bus stop, OR bus ride from A to B                |
| **Route**          | Public transport line metadata (bus/tram/metro number and name)            | Bus "550 Helsinki - Espoo Express"                          |
| **Routing**        | The process of calculating possible itinaries between two points.                           | Finding all ways to get from home to work                   |
| **Transport Mode** | Method of transportation in a leg.                                                         | WALK, BUS, TRAM, SUBWAY, RAIL, FERRY, BICYCLE, CAR          |
| **AI Insight**     | 1-2 sentences of real-world context about an itinerary or leg. | "Bus usually not crowded at this time. 47 social mentions." |
| **Origin**         | Starting point (latitude/longitude).                                                       | Home: 60.1699, 24.9384                                      |
| **Destination**    | Ending point (latitude/longitude).                                                         | Work: 60.2055, 24.6559                                      |
| **Place**          | Named location with coordinates.                                                           | "Kamppi Bus Stop" at 60.169, 24.938                         |

## Journey Metrics

| Term                      | Definition                                           | Example                         |
| ------------------------- | ---------------------------------------------------- | ------------------------------- |
| **Duration**              | Time in seconds for a leg or full itinerary.         | 2700 seconds = 45 minutes       |
| **Distance**              | Length in meters for a leg.                          | 15,000 meters = 15 km           |
| **Walk Distance**         | Total walking in an itinerary (sum of walking legs). | 500 meters total                |
| **Walk Time**             | Total walking time in an itinerary.                  | 400 seconds = 6.7 minutes       |
| **Earliest Departure**    | Desired journey start time.                          | "2025-10-14T12:00:00Z"          |
| **Number of Itineraries** | How many alternative journey options to return.      | 3 different options from A to B |

## Quick Reference

### ❌ WRONG Terminology

- ~~"route"~~ when meaning **itinerary**
- ~~"routes API"~~ when meaning **Routing API** (external HSL)
- ~~"route"~~ when meaning **leg**
- ~~"ai enhancement"~~ or ~~"ai description"~~ when meaning **ai insight**

### ✅ CORRECT Usage

- "The **routing service** performs **routing** to fetch **itineraries** from the HSL **Routing API**"
- "Each **itinerary** contains multiple **legs**"
- "This bus **leg** uses **route** line '550'"
- "Call our **Routibg API** at `/api/v1/routing/search` to get **itineraries**"
- "This **leg** has an **AI insight** about crowding (47 mentions)"
