# Eval Skills for AI Coding Agents

Skills that teach AI coding agents to help you build LLM evaluations: find failures, measure them, and fix them. Each skill is a focused instruction set that an agent loads for a specific eval task.

These skills assume familiarity with eval concepts. They complement the [AI Evals course](https://maven.com/parlance-labs/evals?promoCode=evals-info-url) by Hamel Husain and Shreya Shankar. If you're new to evals, see [questions.md](questions.md) for free articles, videos, and talks on the fundamentals.

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

These skills are a starting point. You'll get better results writing skills that encode your own workflows, domain knowledge, and constraints. Generic skills can't capture what's specific to your product: your failure modes, your data formats, your quality bar. Practitioners who build a small set of bespoke skills grounded in their own data consistently outperform those who rely on off-the-shelf bundles. Start here, then iterate toward custom skills.

## Beyond These Skills

Evals are a human-in-the-loop process. These skills cover the core loop of finding failures, measuring them, and building review tools, but much of eval work is domain-specific and resists generic instruction. For example:

- **CI/CD integration.** Wiring evaluators into deployment pipelines.
- **Production monitoring.** Running evaluators on live traffic and alerting on drift.
- **Prompt and pipeline optimization.** Prompt refinement, task decomposition, model cascades, fine-tuning.
- **Multi-turn and agentic evaluation.** Evaluating chatbots, tool-calling agents, and multi-step pipelines.
- **Annotation rubric design.** Building rubrics with inter-annotator agreement measurement.
- **Code-based evaluators.** Deterministic checks (regex, schema validation, execution tests) for objective failure modes.

These areas depend heavily on your stack, your users, and your failure modes. General skills don't serve them well. The [course](https://maven.com/parlance-labs/evals?promoCode=evals-info-url) covers all of them.
