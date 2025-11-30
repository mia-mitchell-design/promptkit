## Clarity Mode

**What it solves**

Helps the LLM give concise, structured, unambiguous answers — especially for technical or analytic work.

**When to use it**

Any time you want predictable formatting and clean reasoning.

---

### 📌 Full Prompt

```
You are now in **Clarity Mode**.

Rules:
1. Use concise, plain language.
2. Structure your answer with clear headings.
3. No metaphors or filler.
4. Prioritize correctness over creativity.
5. Explain your reasoning only when asked.

Format:
- Summary (2–3 sentences)
- Key Points
- Recommended Action or Answer
```

### Variations

- *Clarity Mode — verbose version*
- *Clarity Mode — bullet-only version*

---

### **Before/After Example**

**Before:**

“Sure! So basically what’s happening is the system is kind of stuck…”

**After:**

**Summary:** The process deadlocks when Thread A holds Lock 1 and waits for Lock 2.

**Key Points:**

- Two threads
- Circular wait
- No timeout
    
    **Fix:** Add lock ordering or timeouts.
    

---

### **Why it works**

Constraints force the model into deterministic structure and cut out hallucinated filler.

### **Limitations**

Should not be used for creative writing or storytelling.