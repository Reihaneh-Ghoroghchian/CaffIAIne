










## 2. `ARCHITECTURE.md`

```markdown
# Architecture Overview

Below, sketch (ASCII, hand-drawn JPEG/PNG pasted in, or ASCII art) the high-level components of your agent.

## Components

1. **User Interface**  
   - E.g., Streamlit, CLI, Slack bot  

2. **Agent Core**  
Agent Core
├── 1. Planner:
│    └── Sequence the tasks:
│        - Get weather
│        - Access closet
│        - Prepare prompt/images for Gemini
│        - Ask Gemini for outfit
│        - Return suggestion
│
├── 2. Executor:
│    └── Executes each tool call and prompt in sequence or parallel
│
├── 3. Memory (optional):
│    └── Caches previous forecasts or user preferences


3. **Tools / APIs**

├── Weather Tool:
│ └── Calls OpenWeatherMap or similar API to get forecast
│
├── File Access Tool:
│ └── Reads from user’s Google Drive / Firebase Storage / Cloud Storage
│ └── Loads images of available clothes
│
├── Gemini API:
│ └── Gemini Pro Vision — receives:
│ - The forecast
│ - Images of clothing
│ - Prompt to decide the best combination


4. **Observability**  
  Output Generator
└── Presents:
- Recommended outfit (text and optional visual layout)
- Reasoning ("because it's rainy and 15°C…")

