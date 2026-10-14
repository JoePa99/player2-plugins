# Player 2

Your company's companyOS, team, skills and brand from Player 2: answers and work grounded in how your company runs, finished work and follow-ups saved back to Player 2, companyOS changes suggested for an admin, and bots Player 2 suggests setting up.

[Player 2](https://player2.si) keeps each company's companyOS: how it thinks, sells, signals, operates, decides, and where it stalls, along with its team, skills, brand and files. This plugin lets Grok Bot and Cursor work from it, live. Nothing about any company is in this repo; everything is read from Player 2 for whoever signs in.

## Setup

1. Install the Player 2 plugin from the Marketplace.
2. When it connects, Player 2 opens its sign-in page. Sign in with your Player 2 login, tick the companies this assistant may reach, and press Allow. No key or header is needed (OAuth with PKCE).
3. In Grok Bot, ask it to make a bot called "Player 2" for your work. The first time that bot uses Player 2, it saves the standing rule that makes it read Player 2 before any work.
4. Try "What does Player 2 suggest?" or "Write a proposal for <client>, on brand."

You need a Player 2 account. Player 2 is by invitation: ask the person who set up your company's Player 2, or write to hello@upupdndn.ai.

## What it includes

- **The Player 2 connector** (`mcp.json`): https://player2.si/mcp, a remote MCP server.
- **Skill `player2`:** when to use Player 2, reading the companyOS fresh, doing work with the company's own skills and brand, and what to send back (changed facts for an admin, real follow-ups, work only when asked).
- **Skill `player2-bots`:** turning the bots Player 2 suggests into running bots.

## Tools

| Tool | What it does |
|---|---|
| `companyos_list_companies`, `companyos_overview`, `companyos_search`, `companyos_read` | Read the companyOS of the companies you ticked |
| `skills_list`, `skill_read`, `brand_read` | The company's own skills and brand |
| `team_list`, `teammate_read` | The company's team in Player 2 |
| `files_search`, `file_read` | The company's files in Player 2 (only the folders you can see there) |
| `memory_read`, `memory_save` | Your own Player 2 memory (never shared) |
| `tasks_list`, `task_add` | Your own Tasks page |
| `clients_read` | The company's clients in Player 2 |
| `work_list`, `work_read`, `work_save` | Work Player 2 made for you; save a piece when you ask |
| `player2_make`, `player2_make_status` | A PDF, deck or document in the company's brand |
| `player2_home` | What Player 2 suggests doing next |
| `companyos_update`, `companyos_undo`, `companyos_history` | Suggest a companyOS change; an admin decides it in Player 2 |
| `teammate_propose` | Suggest a teammate; a person decides it in Player 2 |

## Your data

The assistant reaches only the companies you ticked, and only while you're a member. Members read and suggest; admins of a company decide every companyOS change in Player 2, and nothing is deleted from here. Disconnect any time on the companyOS in your AI page in Player 2.

Support: https://player2.si/support · Privacy: https://player2.si/privacy · Terms: https://player2.si/terms

## License

MIT (this plugin's files). Player 2 itself is a hosted service.
