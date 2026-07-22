# Bots & Automation

Target stack: **3–5 bots**. More adds noise and permission risk.

## The stack

| Job | Bot (pick one) | Why |
|---|---|---|
| Moderation + automod + logging | **Dyno** or **YAGPDB** | Stable, free core, full logging to `#mod-logs` |
| Reaction roles + embeds + tags + scheduled messages | **Carl-bot** or **Sapphire** | Best-in-class self-assign roles; Sapphire is nearly all free |
| Leveling & activity rewards | **Arcane** | Free XP/leaderboards for chat *and* voice; auto role rewards |
| Welcome + invite tracking | **ProBot** or **Invite Tracker** | Custom welcome images; captcha verification during raids |
| Economy / fun (optional) | **UnbelievaBoat** or **Dank Memer** | Server currency + games keeps chat alive between seasons |

## Permission policy (non-negotiable)

- **No bot gets Administrator.** Ever. Grant only what each bot needs.
- **Bot roles sit below all mod/admin roles** in the role hierarchy.
- **No bot or webhook can post in `#announcements`.** Impersonation of admin
  announcements is the #1 NFT-server attack vector. Only human mods post there.
- Review each bot's role permissions quarterly; remove anything unused.

### Minimum permission sets

| Bot | Needs | Does NOT need |
|---|---|---|
| Dyno / YAGPDB | Manage Messages, Kick, Ban, Timeout, Manage Roles (below mods), View Audit Log, Send Messages in `#mod-logs` | Administrator, Manage Server, Manage Webhooks |
| Carl-bot / Sapphire | Manage Roles (below mods), Send Messages, Embed Links, Add Reactions, Manage Messages (for reaction roles) | Administrator, Ban/Kick |
| Arcane | Send Messages, Manage Roles (for level roles only) | Administrator, Manage Messages |
| ProBot / Invite Tracker | Send Messages, Embed Links, Attach Files, View Invites (Manage Server is required for invite tracking — accept this one trade-off or skip invite tracking) | Administrator |
| UnbelievaBoat / Dank Memer | Send Messages, Embed Links, Add Reactions | Administrator, any moderation permission |

## Discord-native security (do this before adding any bot)

1. **Enable Community** — Server Settings → *Enable Community*. Unlocks
   AutoMod, onboarding, Stage channels, Server Insights.
2. **AutoMod** — enable built-in spam + mention-spam + phishing/scam link
   filters, then add the custom keyword rules from
   [`../automod/keyword-rules.md`](../automod/keyword-rules.md).
3. **Verification level Medium/High** — Server Settings → Safety Setup.
4. **DMs off by default** — Discord can't force this server-wide for
   members, so the welcome message instructs everyone to disable server DMs
   (most Axie scams are DM impersonation of "support").

## Automation recipes

### Onboarding auto-roles (Discord native — no bot needed)
Set up per [`../copy-paste/onboarding-questions.md`](../copy-paste/onboarding-questions.md):
"Which games do you play?" → auto-assigns `Origins`, `Classic`,
`Atia's Legacy` roles, which unlock the matching channels. The server only
fully unlocks after onboarding is completed.

### Arcane level roles
| Level | Role | Reward |
|---|---|---|
| 5 | `Axie Regular` | Cosmetic name color |
| 15 | `Lunacian` | Cosmetic name color + image perms in `#memes` if restricted |
| 30 | `Veteran` | Access to a members-only lounge channel |

Enable XP for **both chat and voice** so voice-night regulars aren't
invisible on the leaderboard.

### Scheduled messages (Carl-bot / Sapphire)
- Friday, 2 hours before game night: *"Friday Arena Night in 2 hours — hop
  in the Lobby! 🎮"* (see
  [`../copy-paste/announcement-templates.md`](../copy-paste/announcement-templates.md))
- Season start/end reminders tied to the Origins calendar.

### Logging
Point ALL bot logging (joins/leaves, message deletes/edits, bans, timeouts,
AutoMod triggers, role changes) at `#mod-logs`. One channel, everything in it.
