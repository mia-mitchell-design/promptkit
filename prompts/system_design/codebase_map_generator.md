## Codebase Map Generator

*Produces a visual “mental map” of the repo to supplement the Codebase Explorer.*

**What it solves**

Turns a messy repository into a clean architectural map so you can understand systems at a glance.

**When to use it**

When you want an **executive-level understanding** of the codebase without reading everything manually.

---

### 📌 Full Prompt

```
Generate a **Codebase Map** for the project described below.

Requirements:
- Summarize high-level architecture
- Group files into meaningful subsystems
- Identify main data flows and control flows
- Show how components depend on each other
- Identify the “center of gravity” of the project
- Summarize how state is passed or updated
- Point out missing documentation or unclear boundaries

Format:
1. High-Level Architecture
2. Subsystem Map
3. Data Flow Diagram (written)
4. Control/Event Flow
5. Component Responsibilities
6. Dependency Hotspots
7. Suggested Refactoring Targets
8. Missing Docs / Questions to Ask
```

### Variations

- *Map with ASCII diagram*
- *Map focusing only on backend*
- *Map focusing on data models*

---

### Why it works

It forces the LLM to reason spatially and structurally — essentially producing a “city map” of the system.

### Limitations

May need iterative refinement for large repos.