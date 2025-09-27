---
marp: true
theme: default
paginate: true
---

<style>
.columns {
  display: flex;
  gap: 20px;
}
.column {
  flex: 1;
}
.column-centered {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
}
</style>
<!--
Presenter notes:
Welcome everyone to this session on AI assisted. Today we'll explore how to leverage AI to enhance your development workflow.
-->

Here is the new structure.

First, an introduction where I say what I do. Then I present the outline: I will explain how the whole process works from my experience and what I've seen working, including how people can be proactive at various stages of development. At the end, I will demo the workflow.

I'll start by going through the roots file. The roots file specifies the roots for the LEM and serves as the onboarding document for your agent. Think of your agent like a new team member you are onboarding. I'll show the root file and explain how to structure prompts and what to include.

Next I'll explain the main workflow: Research, Plan, Act. First, ask the LEM to research—find information and fetch documentation via MCP if needed. Then ask it to plan; I typically prompt it to learn about a library and plan how to integrate it or how a refactoring should work. Finally, ask it to implement the plan.

I'll also cover integrations and the environment setup. Web integrations can come before the Research–Plan–Act flow. Set up the environment for the agent to run in, let it interact with that environment, and include a feedback loop for tasks in the Plan–Act stage. Explain what MCPs are useful for and how they fit into the workflow.

Finally, I'll do an end-to-end demo: create an issue, let the agent produce a PR, review the PR, and merge it. That will be the conclusion, organized into two main sections.

# AI Assisted Coding

<div class="columns">
  <div class="column-centered">
    ~You're absolutely right!~
    </br></br>
    How to have fun and ship fast with AI Agents
  </div>
  <div class="column">
    <img src="image.png" alt="Cartoon of farmer teaching horse to drive a tractor">
  </div>
</div>

---

# About Me

<div class="columns">
  <div class="column">
<ul>
<li>Building, simulating, evaluating and deploying AI Agents @Parloa</li>
<li>Chemist -> MLE -> MLOps -> SWE</li>
<li>Hooked on AI in general and especially AI Driven Development</li>
</ul>
  </div>
  <div class="column-centered">
    <img src="1757103512240.jpeg" alt="Presenter Photo">
  </div>
</div>

---

<!-- 
Presenter notes:
Start by explaining the fundamental shift in how we approach coding with AI assistants.
Ask participants to share their current experiences with AI coding assistants.
-->

# Goals

- **Learn** how to prompt AI tools to perform daily development tasks
- **Optimize** your workflows using rule files and commands
- **Reflect** On which possibilities this opens for you in your day to day work

---

<!-- 
Presenter notes:
This session will run for approximately 45 minutes
Encourage participants to ask questions throughout - consider using polls or interactive elements at key points.


-->

# Content Overview

- Setting up Memory Files
- The Plan / Act Workflow
- Commands
- Building Complex Features
- Where to go from here

---

<!-- 
Presenter notes:
Here we take a look at the main basic cloud features and their usage, and how you bootstrap and plan them.

Before we delve into an example.
-->

# Setting up

- Improving agent outcomes by providing specific guidelines
- Define project-specific patterns and recipes:
  - "Follow the repository structure, business logic go into domain/ adapters into adapters/"
  - "Use tdd, start from the test, watch it fail, iterate until fixed"
- Demo: Try again the implementation this time with the rule files

---

<!-- 
Presenter notes:
Demonstrates a simple backend implementation and usage of a feedback loop

TODO: maybe I can let it cook a simple frontend with it to demonstrate how one would go about it.
-->

# The Plan / Act Workflow

* My main day-to-day workflow
* Demo: Implementing in-memory version of a flight booking API

---
<!-- 
Presenter notes:
CLAUDE.md help establish patterns for how AI should behave. This section covers practical examples.
According to research, consistent code styles increase maintainability by 31%.
-->


<!-- 
Presenter notes:
Show how to set up claude to help with PR creation. This saves time on routine tasks.
Have a real PR example ready to demonstrate.
-->

# Commands

* Writing Tickets using EARS requirements
* Preparing PRs

---

# MCPs

- Fetch documentation snippets context7
- Chrome Web Tools for browser

---

# Planning Complex Features

- Spec Driven Development

---

<!-- 
Presenter notes:
MCP (Model Context Protocol) allows integration with external tools like Jira. Show practical examples.
Integration between tools can save up to 5 hours per week according to productivity research.
-->

<!--


[mcp_servers."chrome-devtools"]
command = "npx"
args = ["chrome-devtools-mcp@latest"]

codex mcp add chrome-devtools -- npx chrome-devtools-mcp@latest
claude mcp add context7 -- npx -y @upstash/context7-mcp@latest

 -->
---

# Where to go from here

- Use Plan/Act, iterate a lot on the plan
- Sub Agents