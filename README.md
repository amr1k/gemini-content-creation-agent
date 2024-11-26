# Automated Content Creation with Google Gemini using CrewAI

This notebook demonstrates an automated content creation workflow using CrewAI, leveraging Gemini and several custom tools.  The workflow orchestrates a team of AI agents to monitor financial news, analyze market data, generate content, and perform quality assurance.

![alt text](./images/architecture.png?raw=true)


# API Keys
This project requires the following API keys:

LANGTRACE_API_KEY: For tracing the execution flow (optional, but recommended).

GEMINI_API_KEY: For accessing Google's Gemini large language model.

SERPER_API_KEY: For searching the internet for content

# Data Structures
Defines Pydantic models for structuring the output data:

**SocialMediaPost:** Represents a social media post with platform and content fields.

**ContentOutput** Represents the final output with an article (markdown) and a list of social_media_posts.
Agents and Tasks
Defines four AI agents, each with a specific role and goal, and corresponding tasks:

**market_news_monitor_agent:** Monitors financial news for a given subject.

**data_analyst_agent:** Analyzes market data related to the subject.

**content_creator_agent:** Creates content based on insights from the previous agents.

**quality_assurance_agent:** Reviews and refines the generated content.

Each agent is assigned a task with a clear description, expected output, and optional dependencies on other tasks.

# Crew Execution
Creates a Crew consisting of the defined agents and tasks. The kickoff function starts the workflow. The inputs dictionary provides the subject for content creation. See the notebook for the full code.

# Running the Notebook
Ensure you have the required API keys set in your environment variables or .env file.
Install the dependencies listed in requirements.txt.

## Run the notebook cells sequentially.
This README provides a high-level overview of the notebook's functionality. Refer to the notebook itself for the complete code and detailed comments.