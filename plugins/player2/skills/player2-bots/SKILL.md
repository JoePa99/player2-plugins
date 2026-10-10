---
name: player2-bots
description: "Use when the person asks what bots or routines to set up for their company, says yes to a bot Player 2 suggested, or asks to set up Player 2. Turns Player 2's bot suggestions into a running bot: its name, job, instructions drawn from the companyOS, the company's skills, its schedule and the connectors it needs."
---

# Bots from Player 2

Player 2 watches the person's calendar, inbox, meetings, tasks and recent work against their company's companyOS, and suggests always-on bots worth running: a Friday check of overdue invoices, a Monday pipeline review, a daily read of new client mail against the companyOS.

## Find the suggestions

Call `player2_home` (pass `company` when there are several). Its reply ends with **Bots you could set up**, each with:

- a name and the job it does
- why now: what Player 2 saw that makes it worth running
- when it runs
- the company's skills it uses, and the other connectors it needs (Gmail, Calendar, Drive...)
- its instructions

Show the person the ones that fit, in a line each, and ask which they want. Never set one up without their yes.

## Set one up

After their yes:

1. Create the bot with the suggested name. Its instructions are the suggested ones; keep the lines that tell it to read the companyOS, follow the named skill and save its output back to Player 2.
2. Add the routine on the suggested schedule, in the person's time zone. Ask if the schedule isn't clear.
3. Check the connectors it needs are installed. If one isn't, tell the person which and stop there: they add it themselves.
4. Run it once now, so the person sees what it does, and show them the result.
5. Tell Player 2 it's set up: call `player2_suggestion` with the company, the suggestion's `id` and `action: "started"`, so it isn't suggested again.

If the person says no to one, call `player2_suggestion` with `action: "not_useful"`.

## Every bot's run

Every bot set up from Player 2 follows the `player2` skill: read the companyOS first, use the company's skill for the work, stay on brand, save finished work with `work_save`, put follow-ups on the Tasks page with `task_add`, and suggest companyOS changes it finds (`unattended: true`) for an admin to decide. Nothing is sent, posted, paid or deleted without the person's yes: a bot drafts, the person sends.

Connectors and sign-ins are shared by every bot on the person's account, so a bot set up for one company can reach the others on their Player 2 connection. Give each bot one company in its instructions, and keep its work in that company.
