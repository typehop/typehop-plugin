---
name: dictation-recap
description: Recap the user's recent TypeHop dictations into decisions, to-dos and ideas. Use when the user asks for a recap, summary, digest or task list of what they dictated today, this week, or over a period, e.g. "what did I dictate today?" or "turn this week's voice notes into a to-do list".
---

# Dictation recap

1. Call `recent_dictations` with `days` matching the period the user asked for (1 for today, 7 for this week). Default to 1.
2. Skip dictations that are plain replies or chat messages with no lasting content (e.g. "sounds good, see you then").
3. Group what is left under:
   - **Decisions**: things the user decided
   - **To-dos**: actions, written as checkboxes (`- [ ]`), with the person or date if the user said one
   - **Ideas**: things to think about later
4. Keep each item to one line, in the user's words. Put the date of the dictation in parentheses when the recap spans more than one day.
5. End with how many dictations you read.

Do not invent tasks or deadlines. If the period has no dictations, say so.
