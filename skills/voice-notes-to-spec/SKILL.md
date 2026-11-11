---
name: voice-notes-to-spec
description: Turn the user's TypeHop voice dictations about a feature, product or project into a structured spec or PRD. Use when the user asks to write up, spec out, or document something they talked through or dictated, e.g. "turn my voice notes about onboarding into a spec".
---

# Voice notes to spec

The user has been thinking out loud with TypeHop. Their dictations are rough, spread over several notes and days, and sometimes contradict each other. Your job is to find them and turn them into one clear document.

## Steps

1. **Find the notes.** Call `search_dictations` with two or three different keywords for the topic (product names, feature names, people). If the topic is vague, call `recent_dictations` with `days: 14` and pick the relevant ones. Use `get_dictation` for any note whose text was cut short.
2. **Order them by time.** Later notes win when they disagree with earlier ones. Say so when you resolve a contradiction.
3. **Write the spec** with these sections, leaving out any the notes don't cover:
   - **Problem**: who has it and why it matters, in their words where possible
   - **Goal**: what success looks like
   - **Requirements**: a bulleted list, one requirement per bullet
   - **Out of scope**: things they explicitly ruled out
   - **Open questions**: anything undecided or contradictory
4. **Cite the notes.** After the spec, list the dictations you used with their dates, so the user can check the source.

## Rules

- Use only what the notes say. Do not invent requirements, numbers, dates or owners. If something important is missing, put it under Open questions.
- Keep the user's names for things.
- If no dictations match, say so and suggest the user dictate their thoughts with TypeHop first.
