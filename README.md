---
title: SchemaForge
emoji: 🗄️
colorFrom: blue
colorTo: gray
sdk: static
pinned: false
---

# SchemaForge — Text-to-SQL Synthesizer & Query Profiler

A developer workbench that translates natural language requests into optimized SQL against user-provided database DDL schemas, performing static performance linting and index recommendations.

## Features
- **DDL-Aware SQL Synthesis:** Grounded generation matching entity relational schemas.
- **Client-Side Static Performance Linting:** Real-time checks for unbounded projections (`SELECT *`), missing `LIMIT` bounds, and accidental Cartesian joins.
- **AI Query Profiling:** Generates execution strategy explanations, query complexity scores, and recommended compound indexes via Gemini 3.8 Flash.
- **Zero-Backend Infrastructure:** Direct client-to-API communication with local key persistence.