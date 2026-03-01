# Eval Skills for AI Coding Agents

Skills that guide AI coding agents to help you build LLM evaluations.

These skills assume familiarity with eval concepts. They complement the [AI Evals course](https://maven.com/parlance-labs/evals?promoCode=evals-info-url) by Hamel Husain and Shreya Shankar. If you're new to evals, see [questions.md](questions.md) for free resources on the fundamentals.

## Installation

Tell your AI agent to install the skills from this repo. In Claude Code:

> Install the eval skills plugin from hamelsmu/evals-skills

Or install manually:

```bash
# Add the marketplace
/plugin marketplace add hamelsmu/evals-skills

# Install the plugin
/plugin install evals-skills@hamelsmu-evals-skills
```

To upgrade:

```bash
/plugin update evals-skills@hamelsmu-evals-skills
```

## Available Skills

| Skill | What it does |
|-------|-------------|
| error-analysis | Guide the user through reading traces and categorizing failures |
| generate-synthetic-data | Create diverse synthetic test inputs using dimension-based tuple generation |
| write-judge-prompt | Design LLM-as-Judge evaluators for subjective quality criteria |
| validate-evaluator | Calibrate LLM judges against human labels using data splits, TPR/TNR, and bias correction |
| evaluate-rag | Evaluate retrieval and generation quality in RAG pipelines |
| build-review-interface | Build custom annotation interfaces for human trace review |

Invoke a skill with `/evals-skills:skill-name`, e.g., `/evals-skills:error-analysis`.

## Write Your Own Skills

These skills are a starting point. You'll get better results writing skills that encode your own workflows, domain knowledge, and constraints. Skills grounded in your own data will vastly outperform these generic skills. Start here, then iterate toward custom skills.

The [meta-skill](meta-skill.md) can help you ground custom skills. It works best alongside the context provided in the [course](https://maven.com/parlance-labs/evals?promoCode=evals-info-url).

## Beyond These Skills

These skills handle the parts of eval work that generalize across projects. Much of the process doesn't: production monitoring, CI/CD integration, data analysis and more. The [course](https://maven.com/parlance-labs/evals?promoCode=evals-info-url) covers all of it.
