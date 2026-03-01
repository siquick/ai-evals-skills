# Eval Skills for AI Coding Agents

Skills that teach AI coding agents how to help you build LLM evaluations — systematic ways to find, measure, and fix failures in AI applications. Each skill is a focused instruction set that an agent loads when you need help with a specific eval task.

These skills assume some familiarity with eval concepts. They're companions to the [AI Evals course](https://maven.com/parlance-labs/evals?promoCode=evals-info-url) by Hamel Husain and Shreya Shankar. If you're new to evals or want to understand the reasoning behind the methodology, see [questions.md](questions.md) for free articles, videos, and talks that explain the fundamentals.

## Installation

The easiest way to install: tell your AI agent to install the skills from this repo. For example, in Claude Code:

> Install the eval skills plugin from hamelsmu/evals-skills

Or install manually:

```bash
# Add the marketplace
/plugin marketplace add hamelsmu/evals-skills

# Install the plugin
/plugin install evals-skills@hamelsmu-evals-skills
```

To upgrade to the latest version:

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

## What's Not Covered

These skills focus on the core eval loop: find failures, measure them, build tools to review them. They don't cover:

- **CI/CD integration** — wiring evaluators into your deployment pipeline
- **Production monitoring** — running evaluators on live traffic and alerting on drift
- **Prompt and pipeline optimization** — systematic techniques for improving accuracy and reducing cost (prompt refinement, task decomposition, model cascades, fine-tuning)
- **Multi-turn and agentic evaluation** — evaluating chatbots, tool-calling agents, and multi-step pipelines
- **Annotation rubric design** — building rubrics with inter-annotator agreement measurement
- **Code-based evaluators** — writing deterministic checks (regex, schema validation, execution tests) for objective failure modes

The [course](https://maven.com/parlance-labs/evals?promoCode=evals-info-url) covers all of these.

## Write Your Own Skills

These skills are a starting point, not the destination. You'll get better results by writing skills that encode your own workflows, domain knowledge, and constraints. Generic skills can't capture what's specific to your product — your failure modes, your data formats, your quality bar. Practitioners who design a small set of bespoke skills grounded in their own data consistently outperform those who rely on large bundles of off-the-shelf ones. Start here, then iterate toward custom skills. See [meta-skill.md](meta-skill.md) for guidelines on writing good skills.
