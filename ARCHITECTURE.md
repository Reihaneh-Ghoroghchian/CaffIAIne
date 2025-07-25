










## 2. `ARCHITECTURE.md`

```markdown
# Architecture Overview

Below, sketch (ASCII, hand-drawn JPEG/PNG pasted in, or ASCII art) the high-level components of your agent.

## Components

1. **User Interface**  
   - E.g., Streamlit, CLI, Slack bot  

2. **Agent Core**  
   - **Planner**: how you break down tasks  
   - **Executor**: LLM prompt + tool-calling logic  
   - **Memory**: vector store, cache, or on-disk logs  

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
   - Logging of each reasoning step  
   - Error handling / retries  

