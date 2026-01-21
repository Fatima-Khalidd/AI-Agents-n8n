1.  GMAIL AI-AGENT
The AI Agent uses:

 OpenAI for chat. 
 
 API key from OpenAI website. 
 
 Base URL: https://api.groq.com/openai/v1
 
 Model: llama-3.3-70b-versatile
 
 Simple Memory.

Automation Task: Sending Gmail.

Trigger: Sending Chat Message.

2. HTTP Request Node- API calls- web scraper and agentic Tools

Accessing tools which are not available in n8n via API calls, MCPS. 

HTTP node is used and API calls in 3 scenarios.

scenario 1:      API call to public API endpoint which does not need any authentication to get some fun little facts about cats (https://catfact.ninja/fact)

Scenario 2:      API call to public API endpoint of weather.org to get latest information about the weather in a specific city which is requested.

Scenario 3:      API call to web scraper called Firecrawl that could intelligently scrape any web pages requested. scraped website : https://techcrunch.com/tag/generative-ai/

Workflow nodes Sequence:

Manual Trigger Node -> HTTP POST Request node (Extracting) -> Wait node (waits for 30 sec) -> HTTP GET Request Node (to check status of tracking) -> if node (take action if status is not completed yet even after waiting for 30 sec, wait node is introduced and looped back to http get request node) -> gmail node (send message node) 
 
