# AutoMod Configuration

Server Settings → **AutoMod** (requires Community enabled).

## Step 1 — Enable Discord's built-in rules

- ✅ **Block Suspected Spam Content**
- ✅ **Block Mention Spam** (set threshold: 5 mentions)
- ✅ **Block Words Flagged by Commonly Flagged Words** (all categories as fits your community)
- ✅ **Phishing / suspected scam links** filter

Response for all: **Block message + send alert to `#mod-logs`**. For the
mention-spam rule, also **timeout for 60 seconds**.

## Step 2 — Custom keyword rule: "Crypto scam bait"

Create a custom keyword rule. Paste the keywords below (AutoMod accepts
wildcards: `*` matches any characters).

**Response:** Block message + alert `#mod-logs` + timeout 10 minutes.
**Exempt roles:** Mods/Admins only. **Exempt channels:** none.

```
free mint
*free mint*
claim airdrop
*airdrop claim*
claim your airdrop
support ticket
*open a ticket*
*submit a ticket*
claim reward
*claim rewards*
whitelist spot
*whitelist now*
limited whitelist
wallet validation
*validate your wallet*
*sync your wallet*
*connect your wallet to claim*
seed phrase
*recovery phrase*
private key
*dm me for help*
*dm for support*
*axie support*
*sky mavis support*
free axie
*free axies*
*free ron*
*ronin giveaway*
*double your*
```

## Step 3 — Custom keyword rule: "Drainer / fake domains"

Scammers register lookalike domains. Block the patterns; allow the real
ones via the rule's allowlist.

**Keywords (block):**

```
*axieinfinity*.app*
*axieinfinity*.xyz*
*axieinfinlty*
*axleinfinity*
*ax1einfinity*
*skymavis*.app*
*skymavls*
*roninchain*.app*
*ronin-wallet*
*roninwallet*.app*
*axie-claim*
*axie-airdrop*
*axie-mint*
*atiaslegacy*.xyz*
*atias-legacy*.app*
```

**Allowlist (the real domains):**

```
axieinfinity.com
app.axieinfinity.com
welcome.skymavis.com
skymavis.com
roninchain.com
wallet.roninchain.com
```

**Response:** Block message + alert `#mod-logs` + timeout 1 hour (a drainer
link is never innocent).

⚠️ Maintain this list: when a new scam domain shows up in `#mod-logs` or a
member report, add its pattern here and post a warning in `#scam-alerts`.

## Step 4 — Verify

Post a test from a non-mod account (e.g. "free mint happening now") in a
test channel and confirm it's blocked and logged to `#mod-logs`.

## Related settings (Safety Setup)

- Verification level: **Medium** (registered >5 min) or **High** (member >10 min)
- Explicit media filter: **all members**
- 2FA requirement for moderation: **on**
