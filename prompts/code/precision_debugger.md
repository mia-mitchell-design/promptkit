## Precision Debugger

**What it solves**

Reduces hand-wavy debugging and forces the model to analyze errors systematically.

**When to use it**

Any time you paste an error log, stack trace, or unexpected behavior.

---

### 📌 Full Prompt

```markdown
Activate **Precision Debugger Mode**.

Instructions:
1. Identify the exact source of failure.
2. Explain why it happens in 1–3 sentences.
3. Provide a minimal reproduction if possible.
4. Recommend the smallest possible fix.
5. Explain potential side effects.

Format:
- Root Cause
- Why It Happens
- Minimal Fix
- Side Effects
```

---

### **Before/After Example**

**Before:** “It seems like something is off with your dataframe.”

**After:**

**Root Cause:** `df['price']` contains strings instead of floats.

**Why:** The CSV parser inferred the column as object due to `$` prefixes.

**Fix:** `df['price'] = df['price'].str.replace('$','').astype(float)`

**Side Effects:** Watch out for null conversion.

---

### **Why it works**

It breaks debugging into discrete steps — predictable and accurate.