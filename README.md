# TypeHop

**Use what you've said out loud.** TypeHop turns your voice into clean text in any app on your Mac, Windows PC or in Chrome. This plugin connects your TypeHop dictations to your AI assistant, so it can search them, read them, and turn your spoken thinking into specs, task lists and recaps.

## What you get

**A connector to your dictations** (read-only), with four tools:

| Tool | What it does |
| --- | --- |
| `search_dictations` | Full-text search over everything you've dictated |
| `recent_dictations` | Your latest dictations, optionally from the last few days |
| `get_dictation` | One dictation in full |
| `list_dictionary` | Your custom dictionary of names and terms |

**Three skills:**

- **voice-notes-to-spec**: "Turn my voice notes about the new onboarding into a spec."
- **find-what-i-said**: "What did I say about pricing last week?"
- **dictation-recap**: "Recap what I dictated today as a to-do list."

## Setup

1. Install the plugin. In Claude Code:

   ```
   /plugin install typehop --marketplace typehop/typehop-plugin
   ```

   In Claude.ai, add it from the plugin directory.
2. The first time a tool runs, you're asked to sign in to TypeHop and press **Allow**. That's it: there's no key to copy.

You need a TypeHop account (free to start at [typehop.com](https://typehop.com)) and some dictations in it. Dictations from the TypeHop Mac app and the TypeHop Chrome extension are saved to your account.

To disconnect, visit [typehop.com/connected-apps](https://typehop.com/connected-apps).

## Privacy

- The plugin connects to one server, TypeHop's MCP server at `https://api.typehop.com/v1/mcp`, over HTTPS, using OAuth 2.1. It sends nothing anywhere else.
- Access is **read-only**: it can search and read your dictations and your dictionary. It cannot create, change or delete anything.
- What is read is what the tools return: the text of your dictations, their dates and ids, and your dictionary terms. TypeHop does not receive your conversation with the assistant beyond the tool calls themselves.
- The skills are plain instructions; they run no code.
- TypeHop's privacy policy: [typehop.com/legal/privacy](https://typehop.com/legal/privacy). Terms: [typehop.com/legal/tos](https://typehop.com/legal/tos).

## Support

Email [support@typehop.com](mailto:support@typehop.com) or see [typehop.com/mcp](https://typehop.com/mcp).

## License

MIT
