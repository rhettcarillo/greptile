# Channel Structure

Target: **fewer, busier channels**. Rule of thumb — if a channel hasn't had a
message in a week, merge it into another one. This layout is ~20 channels
total, which is right for 100–500 members.

Channel topics below are ready to paste into each channel's Topic field.

---

## Category: START HERE

| Channel | Type | Permissions | Topic (paste) |
|---|---|---|---|
| `#welcome` | Text | Read-only (deny Send Messages for @everyone) | Welcome! Start here for a quick tour of the server. |
| `#rules` | Text | Read-only | Server rules — short, numbered, enforced. Read before posting. |
| `#announcements` | Announcement | **Mods only can post; no bots, no webhooks** | Server + Axie news. Mods will NEVER DM you first. |
| `#roles` | Text | Read-only (roles via onboarding/reactions) | Pick your games and interests to unlock channels. |
| `#scam-alerts` | Text | Read-only | ⚠️ Scam warnings. Read the pinned message. Mods will NEVER DM you first. |

Content for these channels lives in `copy-paste/`:
- `#welcome` → [`copy-paste/welcome.md`](../copy-paste/welcome.md)
- `#rules` → [`copy-paste/rules.md`](../copy-paste/rules.md)
- `#scam-alerts` → [`copy-paste/scam-alerts-pinned.md`](../copy-paste/scam-alerts-pinned.md)

## Category: COMMUNITY

| Channel | Type | Notes | Topic (paste) |
|---|---|---|---|
| `#general` | Text | The main hangout. Slowmode 5–10s **only if** spam becomes an issue; otherwise leave it fast. | Everything goes here. The main hangout. |
| `#axie-chat` | Text | | Strategy, meta talk, team builds. |
| `#clips-and-wins` | Text | Source for the weekly shoutout | Screenshots, ranked climbs, brag posts. Weekly shoutouts pulled from here! |
| `#memes` | Text | Keeps `#general` clean | Memes only. Keep it fun, keep it clean. |
| `#introductions` | Text | Optional; mods should aim to give every intro a first reply | New here? Say hi and tell us what you play. |

## Category: AXIE INFINITY

| Channel | Type | Notes | Topic (paste) |
|---|---|---|---|
| `#origins` | Text | | Origins seasons, ladder talk, team comps. |
| `#classic` | Text | Only if the community plays it — merge into `#axie-chat` if quiet | Axie Classic discussion. |
| `#atias-legacy` | Text | Growth hook — hype/news for the upcoming MMO | Atia's Legacy news, theorycrafting, and guild planning for launch. 🔥 |
| `#marketplace-talk` | Text | Enforce: no unsolicited DMs, no OTC deals | Axie trading discussion. NO unsolicited DMs. NO OTC deals — use the official marketplace. |
| `#guides-and-resources` | **Forum** | Pin the best posts; forum format stays organized and searchable | Guides, tier lists, and resources. One topic per post. |

## Category: VOICE

| Channel | Type | Notes |
|---|---|---|
| `Lobby` | Voice | General hangout |
| `Game Room 1` | Voice | Playing together |
| `Game Room 2` | Voice | Playing together |
| `Events Stage` | **Stage** | AMAs and tournaments (requires Community enabled) |

## Category: STAFF (hidden from @everyone)

| Channel | Purpose |
|---|---|
| `#mod-chat` | Mod coordination |
| `#mod-logs` | All bot logging goes here — joins/leaves, deletes, bans, AutoMod hits |
| `#suggestions-review` | Triage member suggestions |

## Category: ARCHIVE (hidden from @everyone)

Move dead channels here instead of deleting them. History stays searchable
for mods, and nothing is lost if a topic revives later.

---

## Consolidation pass

When migrating an existing server to this layout:

1. List current channels and note the last message date for each.
2. Anything quiet for 7+ days: move to `Archive`, or merge its purpose into
   the nearest channel above (e.g. `#team-building` → `#axie-chat`).
3. Post a one-line note in `#announcements` explaining the cleanup — frame
   it as "making the server easier to follow", not a downsizing.
4. Re-check in a month via Server Insights and prune again.
