# First-Week Checklist

Execute top to bottom. Total hands-on time: **~3.5 hours**, spread over the
week if needed. Security items come first on purpose.

## Day 1 — Security foundation (~40 min)

- [ ] **Enable Community features** (30 min total for this block)
      Server Settings → *Enable Community*. Unlocks AutoMod, native
      onboarding, Stage channels, and Server Insights.
- [ ] **Turn on AutoMod scam filters**
      Server Settings → AutoMod → enable the built-in *Block Suspected Spam
      Content* and *Block Mention Spam* rules, plus the phishing/scam link
      filter. Then add the custom keyword rules from
      [`automod/keyword-rules.md`](automod/keyword-rules.md).
- [ ] **Set verification level to Medium or High**
      Server Settings → Safety Setup.
- [ ] **Post + pin the scam warning** (10 min)
      Create `#scam-alerts` (read-only), paste
      [`copy-paste/scam-alerts-pinned.md`](copy-paste/scam-alerts-pinned.md),
      and pin it.
- [ ] **Lock down `#announcements`**
      Only mods can post. Remove webhook/bot posting permission — admin
      impersonation via bot/webhook is the #1 NFT-server attack.

## Day 2 — Channel consolidation (~1 hr)

- [ ] **Restructure channels** to the layout in
      [`docs/channel-structure.md`](docs/channel-structure.md), including
      per-channel topics and permissions.
- [ ] **Create a hidden `Archive` category** and move dead channels there.
      Archive, don't delete — history stays searchable for mods.
- [ ] **Convert `#guides-and-resources` to a forum channel** and pin the
      best existing posts.
- [ ] **Paste rules and welcome content** from
      [`copy-paste/rules.md`](copy-paste/rules.md) and
      [`copy-paste/welcome.md`](copy-paste/welcome.md).

## Day 3 — Onboarding + roles (~30 min)

- [ ] **Set up Discord native onboarding** using
      [`copy-paste/onboarding-questions.md`](copy-paste/onboarding-questions.md)
      — game questions auto-assign `Origins` / `Classic` / `Atia's Legacy`
      roles and unlock the matching channels.
- [ ] **Set DMs-off guidance** — the welcome message already includes the
      "turn off server DMs" instruction.

## Day 4 — Bot stack (~1 hr)

- [ ] **Add the bots** per [`docs/bots-and-automation.md`](docs/bots-and-automation.md):
      Dyno (or YAGPDB) + Carl-bot (or Sapphire) + Arcane, optionally
      ProBot/Invite Tracker and UnbelievaBoat.
- [ ] **Grant only the listed permissions** — no bot gets Administrator, and
      all bot roles sit below mod/admin roles in the hierarchy.
- [ ] **Point all logging at `#mod-logs`**.
- [ ] **Configure Arcane level roles** at levels 5 / 15 / 30 with the
      members-only channel unlock at 30.

## Day 5 — Events + rhythm (~20 min)

- [ ] **Announce the first recurring weekly event** (Friday Game Night)
      using the template in
      [`copy-paste/announcement-templates.md`](copy-paste/announcement-templates.md).
- [ ] **Create it in the Discord Events calendar** as a recurring event so
      members can RSVP.
- [ ] **Schedule the Carl-bot reminder**: "Friday Arena Night in 2 hours."

## Ongoing (monthly)

- [ ] Check **Server Insights**: new-member retention + channel activity.
- [ ] Merge any channel that's been quiet for a week.
- [ ] Post the weekly `#clips-and-wins` shoutout in announcements.
- [ ] At **500 members**: enable Server Discovery.
