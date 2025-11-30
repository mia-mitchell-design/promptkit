## Codebase Explorer

*A prompt for exploring and understanding an unfamiliar codebase.*

**What it solves**

Helps you quickly form a mental model of a new repository — structure, responsibilities, data flow, and where key logic lives.

**When to use it**

When joining a new team, inheriting a project, or reviewing a repo before making changes.

---

### 📌 Full Prompt

```markdown
You are assisting me in exploring an unfamiliar codebase.

Task:
Analyze the code or file structure I provide and help me understand:
1. The purpose of the project
2. High-level architecture
3. Key modules and their responsibilities
4. Data flow or request flow
5. Hidden coupling and implicit dependencies
6. Areas of technical debt or complexity
7. Where to start if I need to make a change

Format:
- Project Summary
- Architecture Overview
- Important Modules
- Data/Request Flow (visual or bulleted)
- Risks & Complexity Hotspots
- Suggested Starting Points
- Questions to Clarify with the Team
```

### Variations

- *Explorer (Deep Dive)*— include deeper questions about patterns, testing strategy, and style consistency
- *Explorer (Lightweight)*— summary-only version
- *Explorer (Focus on X)*— explore only networking, storage, UI, or ML logic

---

### **Before/After Example**

**Before:**

“I’m not sure what most of these files do, but I think the API is in here somewhere…”

**After:**

**Project Summary:** A Flask-based API with task scheduling and Redis caching.

**Important Modules:**

- `api/handlers.py`— request routing
- `core/scheduler.py`— async job runner
- `services/cache.py`— Redis wrapper
    
    **Hotspots:**`scheduler.py`couples tightly to database writes.
    
    **Start Here:** read`handlers.py`→ service layer`→`models`.
    

---

### **Why it works**

It mimics what a senior engineer naturally does: zoom out, map responsibilities, identify coupling, highlight hotspots, and guide you to the right starting point.

### **Limitations**

Depends on you supplying enough context; best used with file trees, module lists, or sample files.  Keep security top of mind.