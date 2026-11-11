---
name: find-what-i-said
description: Find something the user said in a past TypeHop dictation and quote it back. Use when the user asks "what did I say about…", "find my note about…", "when did I mention…", or wants the exact wording of an idea, number, name or decision they dictated earlier.
---

# Find what I said

1. Call `search_dictations` with the most specific words the user gave you (names, numbers, product terms). If nothing comes back, try synonyms, a shorter query, or a single key word.
2. If the user gave a time ("last week", "yesterday"), call `recent_dictations` with a matching `days` and scan those too.
3. Answer with the exact quote from the dictation, its date, and one sentence of context. If several notes match, list the best three, newest first.
4. If the text was cut short in the results, call `get_dictation` with its id to read it in full before quoting.

Quote; don't paraphrase when the user asked what they said. If nothing matches, say so plainly. Never make up a quote.
