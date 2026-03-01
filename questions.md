# Resources for Going Deeper

These skills tell your AI agent *how* to do evals, but not *why*. If you're wondering why binary pass/fail instead of Likert scales, why error analysis before metrics, or why code-based checks before LLM judges, these resources explain the reasoning.

## The Course

The most comprehensive and canonical source is the [AI Evals for Engineers](https://maven.com/parlance-labs/evals?promoCode=evals-info-url) course by Hamel Husain and Shreya Shankar. It covers the full Analyze-Measure-Improve lifecycle: data collection and instrumentation, error analysis methodology, custom evaluator design (code-based and LLM-as-Judge), architecture-specific strategies (RAG, agents, multi-turn), production CI/CD integration, and building data review interfaces. The course is designed for engineers and PMs who ship AI products and want systematic approaches instead of manual spot-checking.

## Free Resources

### Essential Reading

- **[Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/index.html)** — A framework for building eval systems organized into three levels: unit tests with assertions, human and model-based evaluation with tracing, and A/B testing. Demonstrates the approach through a real estate AI case study.

- **[LLM Evals FAQ](https://hamel.dev/blog/posts/evals-faq/)** — Practical answers to the most common questions on implementing evals: how to do error analysis, design application-specific evaluators, build annotation tools, and use eval insights to debug AI systems.

- **[Creating an LLM Judge That Drives Business Results](https://hamel.dev/blog/posts/llm-judge/)** — A step-by-step process for building LLM-based evaluators through "critique shadowing" with domain experts. Covers binary pass/fail judgments, few-shot prompt design, and iterative calibration.

- **[A Field Guide to Improving AI Products](https://hamel.dev/blog/posts/field-guide/)** — Six practices that separate successful AI teams from struggling ones: error analysis, custom data viewers, domain expert involvement, synthetic data, trustworthy evaluations, and experiment-driven roadmaps.

- **[Who Validates the Validators?](https://arxiv.org/abs/2404.12272)** (Shreya Shankar et al.) — Introduces the concept of "criteria drift": users need evaluation criteria to grade outputs, but grading outputs helps users define criteria. This is why error analysis must come before writing evaluators.

### Video

- **[Intro to AI Evals with Lenny Rachitsky](https://youtu.be/BsWxPI9UM4c)** — Hamel and Shreya walk through the eval process end-to-end: start with manual error analysis of production data, categorize failure modes, then build targeted automated evaluators that drive a continuous improvement flywheel.

### Lightning Lessons (free short talks)

- **Error Analysis: The AI Engineer's Best ROI** — [slides](https://docs.google.com/presentation/d/1ZNThtixnbZGPpRcjMs8aGeQbzs-Ixe0mbTfvoaPqn3c/edit) | [video](https://www.youtube.com/watch?v=qH1dZ8JLLdU)
- **The Evals That Made GitHub Copilot Happen** — [slides](https://docs.google.com/presentation/d/13lnoKKO647FNcVpG-eKy7bP6pvzzjM_fPJocW8rx9NQ/edit)
- **Stop Managing AI Projects Like Traditional Software** — [slides](https://www.figma.com/slides/m2QuDvlE8E6VQEcGnotLGH/Burn-your-Roadmap) | [video](https://www.youtube.com/watch?v=R_HnI9oTv3c)
- **Inspect, an OSS Python Library for LLM Evals** — [annotated notes](https://hamel.dev/notes/llm/evals/inspect.html)
