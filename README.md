# SchemaForge — Text-to-SQL Synthesizer & Execution Profiler

SchemaForge translates natural language business inquiries into optimized, ANSI-compliant SQL queries grounded in user-provided DDL schemas, combining deterministic linting with generative index profiling.

## Architecture
1. **Schema Context Injection:** Parses table DDL, foreign keys, and constraints to ensure grounded, hallucination-free join conditions.
2. **Client-Side Anti-Pattern Linter:** Inspects generated SQL for performance bottlenecks:
   - Unbounded scans (Missing `LIMIT` or aggregate filters).
   - Wildcard projection risks (`SELECT *` invalidating index covers).
   - Unconstrained joins (Cartesian product detection).
3. **Execution Profiling (Gemini 3.8 Flash):** Computes query complexity, explains execution strategy, and provides concrete compound index recommendations.

## Tech Stack
- Modern Responsive Web Engine (Pure JavaScript / CSS3)
- Gemini 3.8 Flash Structured JSON Outputs
- Deployed on Hugging Face Spaces

## Live Demo
[SchemaForge Live Space](https://huggingface.co/spaces/YOUR_USERNAME/schemaforge-ai)
