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

- **Learn** how to use AI tools to perform daily development tasks
- **Customize** your workflows using rule files and commands
- **Reflect** On which possibilities this opens for you in your day to day work

---

<!-- 
Presenter notes:
This session will run for approximately 45 minutes
Encourage participants to ask questions throughout - consider using polls or interactive elements at key points.


-->

# Content Overview

- Coding from the CLI
- The Plan / Act Workflow
- Rules and Memory
- Commands
- Building Complex Features
- Where to go from here

---

<!-- 
Presenter notes:
Here we take a look at the main basic cloud features and their usage, and how you bootstrap and plan them.

Before we delve into an example.
-->

# Coding Tools

- How to get started with Claude Code and Codex
- Modes & Permissions
- Steering
- Context Management

---

<!-- 
Presenter notes:
Demonstrates a simple backend implementation and usage of a feedback loop

TODO: maybe I can let it cook a simple frontend with it to demonstrate how one would go about it.
-->

# The Plan / Act Workflow

* My main day-to-day workflow
* Implementing in-memory version

```text
flight-booking-mini
```


<!-- 
Presenter notes:
CLAUDE.md help establish patterns for how AI should behave. This section covers practical examples.
According to research, consistent code styles increase maintainability by 31%.
-->

# Rules and Memory

- Define project-specific patterns and recipes:
  - "Follow the repository structure, business logic go into domain/ adapters into adapters/"
  - "Use tdd, start from the test, watch it fail, iterate until fixed"
  - "Use conventional commits, to open PRs use the gh commandline"

---

<!-- 
Presenter notes:
Show how to set up claude to help with PR creation. This saves time on routine tasks.
Have a real PR example ready to demonstrate.
-->

# Commands

Real-world PR automation with conventional commits:

```text
```


<!-- 
Presenter notes:
Demonstrate how to use github issues. We create a command 
-->

# Example: Github Issues

Write, manage tickets using EARS requirements


---

# Building Complex Features

- spec-driven development

---

<!-- 
Presenter notes:
MCP (Model Context Protocol) allows integration with external tools like Jira. Show practical examples.
Integration between tools can save up to 5 hours per week according to productivity research.
-->

# MCP and Integrations

- get up-to-date documentation with context7


<!-- 
Presenter notes:

example we can verify the thing looks good.
-->

# Example: Browser Automation (Chrome Web Tools MCP)

Feedback loop for frontend, use to check the swagger documentation


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