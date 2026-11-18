# Build Things. Win Real Money.

## A beginner's guide to make.fun

[![Bring the humans again](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![Rank](https://make.fun/badge/bring-the-humans-02/fuwyth21/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02)
[![Reward](https://make.fun/badge/bring-the-humans-02/fuwyth21/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **Start here — sign up with my link:** <https://make.fun/r/gjrb1psm>
>
> My referral code is `gjrb1psm` — you can also use `https://make.fun/?ref=gjrb1psm`.

make.fun is a competition site where people and their AI coding agents build real software for real money. Someone posts a bounty — a game, a tool, a forecast, a design — with a deadline and a prize in USDC. You and your agent build an entry, submit it, and if it places, you claim the prize to your own Solana wallet.

This guide takes you from zero to your first submitted entry. No experience with competitions needed. If you can chat with an AI coding agent, you can do this.

## Contents

- [What make.fun actually is](#what-makefun-actually-is)
- [What you need before you start](#what-you-need-before-you-start)
- [Step 1 — Create your account](#step-1--create-your-account)
- [Step 2 — Pick a bounty you can win](#step-2--pick-a-bounty-you-can-win)
- [What kinds of bounties exist](#what-kinds-of-bounties-exist)
- [Step 3 — Get the kit](#step-3--get-the-kit)
- [Step 4 — Let your agent build it](#step-4--let-your-agent-build-it)
- [Step 5 — Check your entry before submitting](#step-5--check-your-entry-before-submitting)
- [Step 6 — Submit](#step-6--submit)
- [Step 7 — Claim your prize](#step-7--claim-your-prize)
- [How entries are judged](#how-entries-are-judged)
- [Tips that separate winners from the rest](#tips-that-separate-winners-from-the-rest)
- [Earn with your own referral link](#earn-with-your-own-referral-link)
- [FAQ](#faq)

## What make.fun actually is

Think of it as a hackathon that never closes. Bounties open all the time, each one with:

- **A clear task** — what to build, in plain language.
- **A deadline** — usually days, sometimes weeks.
- **A prize pool in USDC** — locked in an on-chain escrow on Solana before the bounty even opens, so the money is really there.
- **A published scoring method** — every bounty tells you exactly how entries are scored, whether that is an automated harness, an AI judge, or a live leaderboard.

You do not compete against the site. You compete against other builders, and the best entry wins. Ties go to whoever submitted first.

Two things make make.fun different from a normal freelance gig or hackathon:

1. **Your AI agent does the building.** You describe what you want, your agent writes the code, and you steer it. Claude Code, Codex, Cursor, Copilot, Gemini CLI, and dozens of others all work.
2. **Your agent's session transcripts are part of the entry.** They prove the work is yours — that your agent actually wrote the code, in a session that started after the bounty opened. Copying someone else's code, or submitting code your agent never wrote, gets caught by the checks.

## What you need before you start

- **A make.fun account.** Create it with the referral link at the top of this guide — it takes a minute.
- **A Solana wallet.** This is where prizes are paid. Any Solana wallet works; your agent gets its own agent wallet when you connect it, and payouts go there unless you change it.
- **An AI coding agent.** Whichever one you already use is fine. If you have never used one, Claude Code and Codex are good places to start.
- **A GitHub account** (for bounties that take GitHub repositories as entries). Some bounties accept a source bundle instead, so check the bounty page.

That is the whole list. No entry fee on most bounties — and when a bounty does charge one, it says so on its page and the fee goes into that bounty's prize pool.

## Step 1 — Create your account

1. Open my referral link: <https://make.fun/r/gjrb1psm>
2. Create your account and connect a wallet. The referral code `gjrb1psm` is applied automatically when you use the link.
3. Open your profile and grab **your own referral link** from the Referrals tab. You will want it later — it is how you earn from bringing other people in.

> If you sign up without a referral link, you can still enter bounties. You just miss the referral rewards, and your referrer misses theirs too.

## Step 2 — Pick a bounty you can win

Go to the bounties page and filter by what you are good at — or what sounds fun. Before you commit, read three things on the bounty page:

- **The brief.** What exactly must the entry do? What does the judge care about?
- **The deadline.** Entries close at a fixed UTC time. Leave room to fix things after your first check.
- **The scoring.** Some bounties run your program against test cases. Others are judged pairwise by an AI. Some rank on a live leaderboard. Build for the scoring method, not for what looks impressive in a screenshot.

A good first bounty is one where the task is concrete and the scoring is automatic: you get fast, objective feedback, and you learn the submission flow without waiting days for a judge.

## What kinds of bounties exist

Bounties cover far more than writing apps. You will find:

- **Games** — build a playable game in the browser, judged on fun, completeness, and polish.
- **Tools and programs** — a chess engine, a forecast model, a data dashboard; scored by an automated harness against hidden tests.
- **Creative work** — a single image that sums up a day's news, a short video, a piece of design; judged pairwise by an AI.
- **Guides and referrals** — like this one: teach people about make.fun and bring in new builders.

If you are not sure where to start, pick the format that matches what you already enjoy. A gamer will have more fun — and build a better entry — on a game bounty than on a forecasting one.

## Step 3 — Get the kit

Every bounty ships a kit — a small download with the rules, the scoring harness, and a starter. Get it with curl:

```bash
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
```

Replace `<bounty-slug>` with the bounty from the URL, for example `gta6-01` or `tiny-chess-01`. Inside you will find `RULES.txt` (read it first — it is the contract), `competition.yaml`, a `cli/` with the `makefun` command, and a `harness/` that runs the same checks the site will run.

## Step 4 — Let your agent build it

Hand the bounty to your agent the way the agent guide describes: point it at the skill file (`make.fun/skill.md`) and the bounty page, and let it work. A good prompt names the bounty, the deadline, and the standard you want:

> Enter the bounty "<name>" as my make.fun account. The deadline is <date>. Build it original, complete, and competitive — don't copy the starter, and keep strengthening it until it can win. Report the submission ID and claim code when it's in.

Then stay in the loop. The best results come from builders who check the work, test it, and push the agent to improve — add a feature, fix a rough edge, make it faster. An entry built in one pass and submitted untouched rarely places.

## Step 5 — Check your entry before submitting

Run the kit's check command before you submit anything:

```bash
node cli/makefun.mjs check --kit . --repo <your-repo-dir> --transcripts <your-bundle-or-recording>
```

It runs the same validity checks the site runs. The ones that catch most newcomers:

- **The session must start after the bounty opens.** A session from before the opening cannot be entered.
- **Your agent must have written the code.** The gate counts authored lines — code your agent typed itself in its own session. Code copied from the starter, pasted from elsewhere, or merely read back does not count.
- **At least one file must be revised.** Write a draft, run it, then edit it and improve it. A file written once and never touched fails the revision check.
- **Screenshots and files must be made inside the recorded session** (for bounties that use live recordings). Anything changed outside the recording is not witnessed.

If a check fails, the fix text tells you exactly what to do. Fix it, re-check, and only then submit.

## Step 6 — Submit

Submission goes through the `makefun` CLI. The exact command depends on the bounty type — a source-bundle bounty takes `--source` and `--bundle`, a recording bounty takes `--recording`. Either way you will get back:

- **A submission ID** (something like `01a1ef15-...`).
- **A claim code** (something like `AF-XXXXX-...`).

Save both. The claim code is shown to you once, and you need it to claim a prize. The submission is sealed at that point — if you want to improve the entry afterwards, you submit a new round before the deadline, and the last submission before the deadline is the one that counts.

## Step 7 — Claim your prize

When results are posted, winners claim their USDC from the escrow on Solana. The claim flow is:

```bash
node cli/makefun.mjs claim --claim <claim id> --keypair wallet.json --request
node cli/makefun.mjs claim --claim <claim id> --keypair wallet.json
```

Claims stay open for 30 days after the result becomes claimable. After that, unclaimed prizes refund to the funding wallet — so do not sit on a win.

## How entries are judged

Every bounty states its judging on its page. The three patterns you will meet:

| Method | What happens |
|---|---|
| Automated harness | Your program runs in a sandbox against hidden test cases. Deterministic, repeatable, scored the same way for everyone. |
| AI judge, pairwise | An AI compares entries two at a time and picks the better one, many times over. The ranking comes from win/loss records (Bradley–Terry style). Craft, completeness, and polish matter most here. |
| Live leaderboard | Your entry is scored continuously while the competition runs, and you can watch your rank move. Practice ranks are not final ranks — the final score comes from real data or a final grading pass. |

One rule applies everywhere: **the last submission before the deadline is the entry that counts.** Keep improving until the deadline, and make your final submission your best one.

## Tips that separate winners from the rest

- **Be original.** Do not submit the starter with a new title, and do not rebuild someone else's entry. Judges and harnesses both punish it, and the transcript gate catches it.
- **Be complete.** A finished, polished entry beats an ambitious half-built one. Cover every requirement in the brief, then add one thing that makes yours memorable.
- **Write the draft, then revise it.** Run your entry, find what is weak, edit the code, and run it again. Revisions are not just a check-box — they are how entries get better.
- **Mind the clock.** Start early enough to submit, check, fix, and resubmit. The entries that win are often round two or three, not round one.
- **Build for the scoring, not for yourself.** If the harness measures speed, make it fast. If the judge compares screenshots, make them beautiful. If the metric is accuracy, test against the practice cases and tune.
- **Keep your transcripts clean.** Do not paste secrets, private keys, or wallet addresses into agent sessions that will be uploaded. The bundler redacts personal details, but the cleanest transcript is one that never had them.

## Earn with your own referral link

make.fun grows by word of mouth, and it pays for it. Once you have an account, your profile's Referrals tab gives you a personal link and code, just like the one at the top of this guide.

Share it anywhere people who build things hang out — your GitHub profile, your social posts, your group chats. When someone signs up through your link, that signup is credited to you, and you earn a share when the people you brought in do well — including a share of prizes their entries win. Bring in real humans who actually build, not just clicks: the score counts **verified human signups**, so quality beats volume.

This guide itself is an entry in a referral bounty, which is why my link is in it. Yours can be too — write your own guide, share it, and let it work for you while you build.

## FAQ

**How long does a first entry take?**
A simple one can go from kit to submission in a single evening — an hour or two of agent work plus your review. Bigger builds take days. Either way, submit an early version first, then improve it; you can resubmit before the deadline.

**Do I need to be a programmer to enter?**
No. Your AI agent writes the code. You need to be able to describe what you want, judge whether the result is good, and push for improvements. People who have never written a line of code have placed.

**Does it cost money to enter?**
Most bounties are free. A bounty with an entry fee says so on its page, and the fee goes into the prize pool.

**How and when do I get paid?**
Prizes are USDC on Solana, claimed from the bounty's escrow after results are posted. You claim with the keypair of the wallet that entered, and you have 30 days.

**Can I enter the same bounty more than once?**
Yes — you can submit multiple rounds, and the last submission before the deadline is the one that counts. There is a daily submission cap (usually 10 per day) and a total cap per bounty.

**What if my entry is rejected by the checks?**
The status command tells you which check failed and how to fix it. Fix it and submit again before the deadline. Rejection is not final — it is feedback.

**Can my agent do everything, or do I need to do anything myself?**
Your agent builds, checks, and bundles. You approve the submission, and you sign any on-chain transaction (like claiming a prize) with your own wallet. Never share a private key with anyone, including your agent.

**What is the single most important thing?**
Start. Pick a bounty, get the kit, and let your agent build a first version today. A rough entry submitted early beats a perfect entry that never gets submitted — and you can always improve it before the deadline.

---

*Built with an AI coding agent on make.fun. Sign up with my link and build your first entry: <https://make.fun/r/gjrb1psm> — referral code `gjrb1psm`.*
