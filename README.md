# Axie Community Server Upgrade Kit

Implementation kit for the **Team 2k + Server Upgrade Guide** (July 2026) — a
do-it-this-week upgrade for a 100–500 member Axie Infinity Discord community.

Everything here is either a step-by-step doc or ready-to-paste content, so the
whole upgrade can be executed in a single evening.

## Where to start

Work through [`CHECKLIST.md`](CHECKLIST.md) top to bottom — it's the
first-week checklist from the guide, expanded with links to the exact file
you need at each step.

## Repository layout

| Path | What it is |
|---|---|
| [`CHECKLIST.md`](CHECKLIST.md) | First-week checklist with time estimates, in execution order |
| [`docs/channel-structure.md`](docs/channel-structure.md) | Full channel layout with per-channel settings, topics, and permissions |
| [`docs/bots-and-automation.md`](docs/bots-and-automation.md) | Bot stack, exact permission grants, and automation recipes |
| [`docs/growth-and-activity.md`](docs/growth-and-activity.md) | Engagement + growth playbook and monthly measurement routine |
| [`copy-paste/rules.md`](copy-paste/rules.md) | Server rules, ready to paste into `#rules` |
| [`copy-paste/welcome.md`](copy-paste/welcome.md) | Welcome message + server tour for `#welcome` |
| [`copy-paste/scam-alerts-pinned.md`](copy-paste/scam-alerts-pinned.md) | The pinned safety message for `#scam-alerts` |
| [`copy-paste/announcement-templates.md`](copy-paste/announcement-templates.md) | Weekly event, shoutout, and season announcement templates |
| [`copy-paste/onboarding-questions.md`](copy-paste/onboarding-questions.md) | Discord native onboarding questions + role mapping |
| [`automod/keyword-rules.md`](automod/keyword-rules.md) | AutoMod configuration: scam keyword lists ready to paste |

## Guiding principles (from the guide)

1. **Fewer, busier channels.** If a channel is quiet for a week, merge it.
2. **Security first.** Most Axie scams are DM impersonation — AutoMod, the
   scam-alerts pin, and locked-down `#announcements` come before anything fun.
3. **Retention beats acquisition.** A consistent weekly rhythm grows the
   server more than any invite campaign.
4. **3–5 bots, minimum permissions.** No bot gets Administrator.
