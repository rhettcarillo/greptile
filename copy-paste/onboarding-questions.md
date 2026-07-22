# Discord Native Onboarding — Questions & Role Mapping

Server Settings → **Onboarding** (requires Community enabled). Configure so
the server fully unlocks only after questions are answered.

## Default channels (visible pre-onboarding)

- `#welcome`
- `#rules`
- `#announcements`
- `#scam-alerts`
- `#general`

## Question 1 — required

**"Which Axie games do you play (or plan to play)?"** *(multi-select)*

| Answer | Role assigned | Channels unlocked |
|---|---|---|
| ⚔️ Axie Infinity: Origins | `Origins` | `#origins` |
| 🃏 Axie Classic | `Classic` | `#classic` |
| 🌏 Atia's Legacy (the MMO — hyped!) | `Atia's Legacy` | `#atias-legacy` |
| 👀 Just here to hang out | `Community` | — (community channels are default) |

## Question 2 — optional

**"What are you into?"** *(multi-select)*

| Answer | Role assigned | Channels unlocked |
|---|---|---|
| 📈 Trading & marketplace | `Trader` | `#marketplace-talk` |
| 📚 Guides & theorycrafting | `Theorycrafter` | `#guides-and-resources` highlighted |
| 🎉 Events & game nights | `Event Enjoyer` | Gets @-mentioned for event pings |
| 🎨 Memes & clips | `Memer` | `#memes`, `#clips-and-wins` highlighted |

## Question 3 — optional

**"Want event notifications?"** *(single-select)*

| Answer | Role assigned |
|---|---|
| 🔔 Yes — ping me for game nights & tournaments | `Events Ping` |
| 🔕 No pings, I'll check the calendar | — |

Use `@Events Ping` (not `@everyone`) for event reminders — keeps
notifications opt-in and complaint-free.

## Notes

- Keep `#roles` as a fallback text channel with Carl-bot/Sapphire reaction
  roles for members who joined before onboarding was enabled.
- Roles created here are **cosmetic + channel-access only** — no
  permissions beyond viewing their channels.
