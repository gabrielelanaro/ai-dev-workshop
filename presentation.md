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

# Cooking Class: How to Work with AI

## My Experience with AI-Assisted Development




---

# About Me

<div class="columns">
  <div class="column">
<ul>
<li>Gabriele Lanaro, "Gabi"</li>
<li>Staff Engineer, Agent Builder Tooling @Parloa</li>
<li>Chemist -> MLE -> MLOps -> SWE</li>
<li>Hooked on AI in general and especially AI Driven Development</li>
</ul>
  </div>
  <div class="column-centered">
    <img src="1757103512240.jpeg" alt="Presenter Photo">
  </div>
</div>

<!-- 
Tell about what the company is about and how long you were there, introduce the story how you got hooked into AI Driven Development
-->

---

# Real Results: Why AI Development Works

## The Impact We Observed
- 60% increase in developer productivity (one team measurement)
- Adoption has grown steadily since March
- Visible inner-sourcing effects across teams (reduced language barrier)

**Takeaway:** Momentum is real—teams ship faster with less friction.
**Bottom line:** It’s not black and white, but you can do things you couldn’t do before.

---

# Today's Agenda

## A basic AI-Driven development workflow

**What I'll cover today:**
- Picking your models
- Basic Context Engineering
- Workflows/Automation

---

# The Agent's Environment: A Developer-Setup Ecosystem

**Key principle:** Let the agent act and self-verify in its environment

**Developer responsibilities:**
- Set up the agent context
- Establish feedback loops: make sure the agent can check its work
- Decide on the requirements and constraints/guidelines

**Agent capabilities within this environment:**
- Research and explore, provide options
- Write code, run tests, self-correct

**Why this matters:** The agent will be much more successful as this is how it was trained.

---

# Picking Your Model

## Anthropic
* Claude Opus 4.1: Favorite among developers
* Claude Sonnet 4: Great model

## OpenAI
* GPT-5-Codex: My Personal Pick

## Notable Mentions
* GLM-4.5 (z-ai): On par with sonnet for 3 euro/month
* Grok Code Fast (x-ai): Fast model for execution


---

# Creating Rules Files (AGENTS.md)

**Key Principle:**: AGENTS.md is the main customization point for your workflows

**What to include:**
- Project structure and architecture patterns
- Coding standards and best practices
- Testing approaches and requirements
- Any type of workaround

**Metaphor**: Agent is a developer starting from scratch every new session

---

# The Plan-Act Workflow

## Plan Phase
- ALWAYS Ask the agent to plan the change
- Guide the agent by asking to gather context
- Limit the scope by being specific: "focus on the e2e tests only"

## Act Phase
- Implement the planned solution
- Iterate based on feedback and testing results

**Tip**: Do not be afraid to start over

---

# PR Preparation

- automate your PR creation
- use pre-commit hooks/pre-push hooks to establish feedback cycle
- use commands to create issues and PRs, so you can have automation end 2 end

---

# Review Process

- Set up coding review bots (Bugbot, codex)
- CAREFULLY review the code, the agents will make very subtle mistakes
- Leave comment in PRs, and address them using the agent

---

# Useful MCPs

**Using MCP for documentation:**
- **context7**: Fetch up-to-date library documentation and examples
- **Integration tools**: Connect with external systems (Jira, GitHub, etc.)

**Examples:**
1. "Research NestJS validation patterns and best practices"
2. "Fetch context7 documentation for @nestjs/common validation decorators"

---

# Key Takeaways

**For your daily workflow:**
- Use Plan/Act approach, iterate extensively on the plan
- Create comprehensive AGENTS.md files for consistent agent behavior
- Build feedback loops for the agent to self-check its work
- Leverage MCP tools for documentation and integration

---

# Down the Rabbit Hole

**Advanced techniques:**
- Sub-agents for complex multi-step tasks
- Background Agents in Slack
- Spec Driven Development https://github.com/github/spec-kit
- BMAD Method https://github.com/bmad-code-org/BMAD-METHOD

---

# Stay Updated

**Questions?**
Let's discuss your specific use cases and challenges!

**Get more AI development insights:**
- Newsletter: [teamkitchen.substack.com](https://teamkitchen.substack.com/)
- Follow for updates on AI-assisted coding and agent development
