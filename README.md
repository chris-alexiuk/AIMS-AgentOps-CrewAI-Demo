# Using AgentOps for Visibility with CrewAI for Financial Analysis - AI Makerspace!

<p align="center">
  <img src="https://images.lumacdn.com/cdn-cgi/image/format=auto,fit=cover,dpr=1,background=white,quality=75,width=400,height=400/event-covers/n1/1e0a4049-ccd4-4ed0-b7ca-a66a192af63c" />
</p>

---

## Introduction:

This repository is meant to showcase the power of [AgentOps](https://www.agentops.ai/) for monitoring, testing, and replay analytics!

To showcase AgentOps, we have built a multi-agent "crew" (powered by [CrewAI](https://github.com/joaomdmoura/crewAI/tree/main)) meant to generate AI-powered financial advisement reports. 

> NOTE: This example does not provide real financial advice and should not be used to guide investment strategy

## Adding AgentOps

You'll notice that the only line of code required to add the entire stack of AgentOps is:

```python
agentops.init(tags=["stock_analysis-crew"])
```

> We will still need an API key - which you can grab following the process made available by the AgentOps team [here](https://docs.agentops.ai/v1/quickstart)!

## Running the Crew!

We'll explore how to run the crew in detail below!

### Step 1: Cloning this Repository!

1. We'll want to start by cloning this repository, which can be done as follows:

```bash
git clone https://github.com/AI-Maker-Space/AIMS-CrewAI-Demo.git
```

2. Next, we'll `cd` into the newly cloned repository:

```bash
cd AIMS-CrewAI-Demo
```

### Step 2: Initializing Our Environment Variables

We'll be using the following APIs to help us today:

1. [AgentOps API Key]()
2. [OpenAI's API for GPT-4 and Text-Embedding-3-Small](https://platform.openai.com/docs/quickstart)
3. [Sec API](https://sec-api.io/)
4. [SerpAPI](https://serpapi.com/)

Once we've collected all our API keys, we can continue to add them to our `.env` file.

1. Next we'll create a new empty `.env` file to store our actual environment variables in.

```bash 
cp .env.sample .env
```

2. We'll add the content and fill in our API keys in the newly created `.env` file.

### Step 3: Install Dependencies through Poetry

We can install our dependencies straightforwardly using Poetry!

```bash
poetry install --no-root
```

### Step 4: Run the Agent Crew!

All that's left to do now is run the crew, which we can do with:

```bash
python main.py
```

After which it will ask for a company and we're off!

### Step 4: 

Head on over to [https://app.agentops.ai/projects](https://app.agentops.ai/projects) and select the project you created with your API key!

At this point, you should be presented with the dashboard, which is filled with tonnes of useful metrics!

![image](https://i.imgur.com/14dzjTs.png)

## Credits:

This repository is largely based on the example from the CrewAI creator [@joaomdmoura](https://x.com/joaomdmoura) and the original can be found [here!](https://github.com/joaomdmoura/crewAI-examples/tree/de183dcab06b8021dd403ec4d07116e4ed9b5da8/stock_analysis)
