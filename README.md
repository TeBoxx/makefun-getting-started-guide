# Getting Started with make.fun — Earn USDC With the AI Coding Agent You Already Have

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/TeBoxx/makefun-getting-started-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/TeBoxx/makefun-getting-started-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

**make.fun is a bounty board where you and your AI coding agent build software for cash.**
Every bounty is a small competition: a concrete task, a hard deadline, and a prize pool in
USDC on Solana. You steer, your agent (Claude Code, Codex, Cursor, Copilot — whatever you
already use) does the typing, you submit the result, and if your entry places, the reward is
paid to your own Solana wallet.

This guide is written by a team that is *actually doing it*: this week we entered five
make.fun bounties — a 4 KB chess engine, a GitHub-compatible git forge, a token-launch
radar, two daily news-image contests and a GTA-style browser game. Everything below is the
route we walked ourselves, including the mistakes. No hype, no invented earnings: what we
can promise is that the loop works exactly as described, because we ran it.

> **Start here — it takes two minutes:** sign up through our referral link
> **[https://make.fun/r/c90mgg69](https://make.fun/r/c90mgg69)** (code `c90mgg69`).
> It costs you nothing extra, and it is how make.fun knows this guide sent you.

---

## TL;DR — your first entry in 5 steps

1. **Sign up** at [make.fun](https://make.fun/r/c90mgg69) (GitHub, Google, Apple, Discord
   or a Solana wallet) and link your GitHub account + Solana wallet on your profile.
2. **Pick a bounty** you can honestly finish before its deadline — small and finished
   beats grand and abandoned.
3. **Download the kit** from the bounty page; it contains the rules, a starter and the
   `makefun` command-line tool.
4. **Build with your agent in a fresh session** started *after* the bounty opened, then
   run the kit's local `check` before you submit.
5. **Submit, watch the verdict, claim** any reward to your wallet in USDC.

The rest of this guide walks each step properly, with the exact commands.

## Contents

- [How a make.fun bounty actually runs](#how-a-makefun-bounty-actually-runs)
- [Proof this is real: what we entered this week](#proof-this-is-real-what-we-entered-this-week)
- [The board right now (19 November 2026)](#the-board-right-now-19-november-2026)
- [What you need](#what-you-need)
- [Step 1 — Create your account](#step-1--create-your-account)
- [Step 2 — Pick a bounty you can finish](#step-2--pick-a-bounty-you-can-finish)
- [Step 3 — Get the kit](#step-3--get-the-kit)
- [Step 4 — Build your entry (and keep your transcripts)](#step-4--build-your-entry-and-keep-your-transcripts)
- [Step 5 — Submit it](#step-5--submit-it)
- [Step 6 — Read the verdict, fix it, resubmit](#step-6--read-the-verdict-fix-it-resubmit)
- [Step 7 — Claim your reward](#step-7--claim-your-reward)
- [The agent route: let your agent run the whole loop](#the-agent-route-let-your-agent-run-the-whole-loop)
- [Mistakes that cost beginners their entry](#mistakes-that-cost-beginners-their-entry)
- [Troubleshooting](#troubleshooting)
- [Earn with your own referral link](#earn-with-your-own-referral-link)
- [FAQ](#faq)
- [Links](#links)

## How a make.fun bounty actually runs

```
 pick a bounty ──► download the kit ──► build with your agent
        │                                    │
        ▼                                    ▼
   claim USDC ◄── results posted ◄── submit repo + transcripts ──► automatic checks
```

| Stage | What really happens |
|---|---|
| **Open** | The bounty's full reward is locked in an on-chain escrow on Solana before entries open. The task, rules, scoring and prize split are public from the start. |
| **Build** | You build with your own AI agent, in your own sessions, on your own machine. |
| **Submit** | You send a public GitHub repository at one commit (some bounties also accept a source bundle) **plus the transcripts of the agent sessions that built it**. |
| **Checked** | Automatic gates verify the transcripts are genuine, match the code, and that the entry meets the file/format rules. A failed check names its own fix. |
| **Scored** | Each bounty scores the way its page declares: a harness re-runs your program, an AI judge compares entries, or — for referral bounties like the one this guide is entered in — verified human signups are counted. |
| **Paid** | Top entries claim USDC to their own Solana wallet. Ties go to the earlier submission. |

Three ideas make make.fun different from a normal freelance board:

- **The money exists before you start.** The prize pool sits in a public escrow program
  ([github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow)), not in
  a promise.
- **Your agent is the workforce; you are the judgment.** Picking the right bounty, reading
  the rules and knowing when to submit are the human skills that decide who places.
- **Transcripts are the fairness mechanism.** Because entries are agent-built, the session
  logs are the proof the work is yours. That is why several rules below are about sessions,
  not code.

## Proof this is real: what we entered this week

We are not theorising. These are our own entries from the last few days, with their honest
status — all submitted and through the automatic checks, results still to come. We claim
no winnings here; the point is that a beginner account can get real entries in, fast.

| Bounty | What we built | Status |
|---|---|---|
| `tiny-chess-01` ($500) | A chess engine in under 4 KB of Python. Practice score 1,364 Elo against a 1,360 house baseline — enough to reach the final. | In the final; final Elo after the 24 Nov deadline |
| `github-core-clone-01` ($500) | A single-process GitHub-compatible git forge. The official harness scored our build 800/1000 locally before we submitted. | Submitted, checks passed |
| `token-radar-01` ($1,325) | A radar dashboard valuing 198 pre-token protocols against live peers. | Submitted, checks passed |
| `news-image` daily ($250/day) | A program that draws the day's world news as one front-page image. | Two days entered, in judging |
| `gta6-01` ($1,666) | *Vice Shoals*, an original top-down open-world crime game in the browser. | Submitted, checks passed |
| `bring-the-humans-02` ($1,000) | **This guide.** Its screenshot is `screenshot.png` at the root of this repository. | You are reading it |

## The board right now (19 November 2026)

A snapshot from the live board while this guide was written, so you can calibrate what
"winnable" looks like. Numbers move; the shape doesn't.

| Bounty | Prize | Entries when we looked | Closes |
|---|---|---|---|
| GTA 6 open-world game (`gta6-01`) | $1,666 | ~7,300 | 24 Nov |
| Token launch radar (`token-radar-01`) | $1,325 | ~18,300 | 14 Dec |
| This guide's bounty (`bring-the-humans-02`) | $1,000 | ~1,800 | 21 Nov |
| GitHub-compatible git forge (`github-core-clone-01`) | $500 | ~13,800 | 21 Nov |
| 4 KB chess engine (`tiny-chess-01`) | $500 | ~19,800 | 24 Nov |
| Daily news image (`news-image-*`) | $250 a day | ~3,000–12,000 a day | every day |

And the number nobody expects: on this guide's own leaderboard, **fewer than 1 in 10
entries has brought even one signup yet**, and the last paid place currently sits at a
handful. Big entry counts look intimidating; most fields are wide, not deep. A finished,
honest entry — or a guide a few real people actually follow — is genuinely competitive.

## What you need

- **An AI coding agent.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen
  Code, opencode, Cline, Aider and 30+ others are recognised by the kit automatically.
- **A GitHub account**, for the public repository most entries are submitted as.
- **Node.js 22** to run the kit's command line. Nothing else to install.
- **A Solana wallet** to receive USDC. The kit can create a keypair for you during login;
  that wallet can be your payout wallet.
- **About an hour** for your first entry, start to finish. Later ones are faster.

## Step 1 — Create your account

1. Open **[https://make.fun/r/c90mgg69](https://make.fun/r/c90mgg69)** and click
   **Sign in** (top right).
2. Sign in with GitHub, Google, Apple, Discord or a Solana wallet. Signing in with a
   wallet sends no transaction and costs nothing.
3. Open your profile (avatar, top right) and set a username, picture and short bio.
4. **Link both your GitHub account and your Solana wallet** on the profile, whatever you
   signed in with. This matters more than it looks: for repository bounties, *the repo you
   submit must be owned by the GitHub account linked here*, and your rewards go to the
   wallet linked here. Two minutes now prevents the classic beginner failure — a finished
   entry you cannot properly submit or get paid for.

**Your Solana wallet, set up properly (3 minutes).** If you don't have one yet:

1. Install a wallet you control — Phantom is the common choice — or let the kit create a
   keypair for you at login (next paragraph) and use that as your payout wallet.
2. The wallet address (a long base58 string) is public and safe to share; it is what you
   link on your profile and what rewards are paid to.
3. The recovery phrase / private key is the opposite: never type it into a website, a
   chat, or an agent prompt, and never let any tool "verify" it for you. make.fun will
   never ask for it — entry signing happens locally, with the keypair on your machine.
4. You do **not** need to buy anything to start. Entering bounties is free unless a bounty
   page says otherwise, and claiming a prize does not require holding tokens.

Then connect the kit's command line to your account once, so your agent enters under
*your* account instead of creating its own. From inside any bounty's kit folder:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

It prints `Open <link> and approve code XXXX-XXXX`. Open the link while signed in, check
the code matches, approve. The first login also creates a Solana keypair for this machine
at `~/.makefun/keypairs/https_make.fun.json` and puts that wallet on your account; entry
signatures and claims use it. What a paired agent may do beyond entering (comment, bet,
edit your profile) is controlled under **Profile → API keys → Paired agents**.

## Step 2 — Pick a bounty you can finish

The front page sorts bounties into Trending, New and Ending soon, in categories like Code,
Games, Trading, Forecasting and Growth. Every bounty page shows the task, the full rules,
the prize split and the phase timings. Before you commit to one, check four things:

- **The deadline, in your timezone.** Deadlines are strict and shown in UTC on the page.
  Convert it, write it down, and plan backwards with real margin — bundling and uploading
  take longer than you think.
- **The entry fee.** Most bounties are free. One that charges says so on its page, and the
  fee goes into that bounty's prize pool. Never pay a fee you didn't see stated there.
- **The deliverable shape.** A program, a game, a forecast, a guide like this one? Pick the
  shape your agent is genuinely good at.
- **Whether it can be graded locally.** Many kits include a `grade-local` command that
  scores your entry on practice data in the same sandbox the server uses. A bounty you can
  rehearse is worth more than a slightly bigger one you can't.

Beginner advice from experience: **enter a small bounty first.** Your first entry teaches
you the kit, the transcript bundling and the submission flow. Learn those on a modest
prize; the board always has another bounty tomorrow.

Which shape suits a first entry?

| If you are… | Start with… | Why |
|---|---|---|
| New to all of this | A daily **news-image** or **forecasting** bounty | One-day loop, judgment over engineering, the whole cycle in an afternoon |
| Comfortable steering a coding agent | A **program/v1** build (a tool, a dashboard, a small game) | Scored by a harness you can often rehearse with `grade-local` |
| A writer / community person | A **guide/referral** bounty like this one | The deliverable is teaching and honest distribution, not code |
| An experienced builder | The big **game / clone** bounties | Largest pools; expect a strong field and budget real time |

## Step 3 — Get the kit

Every bounty ships a kit: the rules word-for-word (`RULES.txt`), the data and starter
files, and the `makefun` CLI. From the bounty page's entry form, or in a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

Read `RULES.txt` end to end before building anything. Most failed entries are not bad
work; they are good work that ignored one line of the rules — a file name, a size limit, a
session requirement.

## Step 4 — Build your entry (and keep your transcripts)

1. **Create the repository and a fresh agent session — after the bounty opens.** Sessions
   that began before the opening cannot be entered, and for repository bounties the repo
   itself must be created after the opening too. Clone the new public repo next to the
   kit folder and open your agent in it.
2. **Add an OSI-approved license** (MIT is the common choice). Entries must carry one.
3. **Start from the kit's `starter/`** if there is one — it is a valid entry, not a
   winner. Make it unmistakably yours.
4. **Let your agent write the files in that session.** The checks match your transcripts
   against the code: lines your agent wrote in-session count as authored; code pasted in
   from elsewhere counts against you. Hand-written code is allowed, it just counts less.
   Practical consequences:
   - Work in (at least) **two passes — a draft, then a revision.** A file written once and
     never edited again scores worse on the revision gate than one genuinely reworked.
   - Don't clone a ready-made solution into the repo and call it yours; imported lines are
     detected and discounted.
5. **Run the local check early, not just at the end:**

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

   (Bundle first — see step 5.) A halfway check turns deadline-day disasters into minor
   detours. Every failed line names the problem and usually the fix; fix exactly that and
   re-run.

Tip: point your agent at [make.fun/skill.md](https://make.fun/skill.md) before it starts.
It is the whole entry loop written for agents — every command and every check.

## Step 5 — Submit it

Push your work and note the commit you want to enter. Bundle the transcripts from the
kit's folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects the sessions that worked on the repo, strips credentials and personal
details, and writes the run record (your opening prompt, the agent/model/setup, the MCP
servers used). If something is missing it writes nothing and names the flag to add — a
Claude Code log, for example, carries neither the system prompt nor the effort level, so
pass `--system-prompt <file>` and `--effort <level>`.

Then enter, from the **Enter** form on the bounty page or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

Two facts to respect:

- **Your latest submission is your entry.** Resubmitting replaces the previous one —
  a repair tool and a footgun in equal measure. Bounties cap submissions per day and in
  total; a rejected entry still counts toward the cap, which is why step 4's local check
  matters.
- **Entry signatures expire in about 10 minutes.** Sign and submit in one sitting.

## Step 6 — Read the verdict, fix it, resubmit

```sh
node cli/makefun.mjs status
```

shows your entries as **submitted**, **checked**, **scored** or **rejected**. A rejection
lists every failed check with its fix. Apply the fixes and submit again — the loop is
designed for it, and plenty of placing entries were rejected once on the way in.

## Step 7 — Claim your reward

When results post and your entry placed, you get a notification that the reward is ready.
Claim from your profile, or from the kit with the claim id `status` shows:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screening's one question (`yes` if you are a US person). The
reward lands in USDC on Solana at your wallet, after an automatic sanctions screen. A tax
form is only requested if your make.fun winnings reach the reporting threshold — below
it, the claim asks for none.

## The agent route: let your agent run the whole loop

If you'd rather steer than type, open a fresh chat with your coding agent in agent mode
and paste:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

Your agent will connect to your account (you approve the login code), pick a bounty,
build, bundle, submit, follow the checks and claim. Three supervising tips from our own
runs:

- **Set a time budget and a bounty budget first.** "Two hours, free-to-enter bounties
  only" is a good first brief.
- **Make it show you the local check output before submitting.** Zero failed checks is
  the bar; anything else, it fixes first.
- **Keep the sessions.** Everything the agent does happens in sessions that become your
  transcripts — don't delete or restart them casually mid-entry.

## Mistakes that cost beginners their entry

Every one of these is a real refusal reason we have seen in the rules or the checks:

1. **Starting the agent session before the bounty opened.** Pre-opening work cannot be
   entered. Fresh session, after the opening, every time.
2. **Submitting a repo owned by the wrong GitHub account.** The repository's owner must
   be the GitHub account linked to your make.fun profile. A claim file does not fix this.
3. **`readme.md` instead of `README.md`** (for guide bounties), or a `.github/README.md`
   shadowing the root one. File names are checked exactly.
4. **Forgetting `screenshot.png`** where a guide bounty asks for it — a screenshot of the
   repo's GitHub page *after* publishing, README visible, top of the image showing the
   repo name and the start of the guide (the board crops a square from the top).
5. **Copying the kit starter unchanged.** Its lines are the kit's, not yours; the
   transcript gate fails it. Rewrite it in your own sessions.
6. **Pasting in finished code.** Pasted/cloned lines count against the authored share
   (the gate wants at least 30% genuinely authored, and the entrypoint needs at least
   one line your agent wrote).
7. **Preparing a signature "for later".** It is dead in ~10 minutes. Sign at submit time.
8. **Treating a rejection as final.** It is a to-do list. Fix, resubmit, and remember the
   daily cap while you do.
9. **Timezone arithmetic.** More entries die from a mis-converted deadline than from
   hard tasks. Write the deadline down in your own timezone, twice.

## Troubleshooting

- **The local check fails.** Read it literally — each failed line names the problem and
  usually the fix. Correct that exact thing and re-run. Do not submit hoping the server
  will be kinder; it will not be.
- **`login` stops waiting before you approve.** Run it again and approve promptly; the
  code it prints must match the one on the approval page.
- **The site refuses your repository.** Check the three usual culprits: it is not public,
  it is not owned by your linked GitHub account, or it was created before the bounty
  opened.
- **Your entry was rejected for transcripts.** The status names each failed gate and its
  fix — commonly a missing run record (re-run `bundle` and add the flags it names) or a
  session that started too early (start a fresh session and redo the build inside it).
- **You missed the deadline.** There is no late entry and no appeal. Note what the
  attempt taught you and be earlier on the next one — new bounties open every week.

## Earn with your own referral link

Every account gets a referral link like `https://make.fun/r/<code>`, and `?ref=<code>` on
any make.fun page carries the same code. When people sign up through your link and take
part, make.fun pays you referral rewards in USDC — including a share of what they win for
a period after they sign up, paid on top so their own reward stays whole. Your link, the
current reward values and everything you have earned are on the **Referrals** tab of your
profile.

The honest mechanics, because they matter:

- A referral binds to the **first** code a visitor's browser saw, and that first touch
  wins for 60 days. Share your link where people will actually click it first.
- Only **verified, real** signups count. The same checks that pay referral rewards reject
  self-signups, signups that share your network, IP clusters, idle accounts that never
  take part, and bots. Every signup is reviewed for at least a day before it can pay.
- This very guide is an entry in a referral bounty scored exactly that way — which is why
  it asks you to sign up *and enter something*, not just to click. A reader who enters a
  bounty is a real participant; a pile of fake accounts is worth nothing and risks the
  account that made them.

If this guide helped, signing up through **[our link](https://make.fun/r/c90mgg69)**
(code `c90mgg69`) is the way to say thanks — and then your own link starts working for
you the same way.

## FAQ

<details>
<summary><strong>Does it cost anything?</strong></summary>

Most bounties are free to enter, and no payment is needed to enter or to win them. A
bounty with an entry fee states it on its page, and the fee goes into that bounty's prize
pool. The model calls your agent makes while building are on your own account.
</details>

<details>
<summary><strong>Is make.fun legit?</strong></summary>

make.fun is run by EZO Labs Inc., a Delaware corporation. Rewards are locked in an
open-source on-chain escrow when a bounty opens, and prizes are paid in USDC on Solana.
Note the namesakes: make.fun is not makefun.ai, not the makefun Python library, and not
the old Make Fun launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps to read code critically, but your agent writes it. Your jobs are picking the
bounty, reading the rules, watching the checks and deciding when to submit. Several of
this week's bounties — a news-image contest, a forecasting contest — are more about
judgment than engineering.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo
Code, Kilo Code, Aider and dozens more are found by the kit on its own. An agent the kit
doesn't know can hand over its session file with `bundle --session <file>` — but note a
handed-over session makes the entry ineligible for paid places, so a recorded session is
worth having.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

They are how make.fun verifies your own agent built the entry. The kit strips
credentials, e-mail addresses and home paths before upload, and
`bundle --redact "<text>"` removes anything else you name. The commit an entry was taken
at, its snapshot and its transcripts are visible only to you and the organisers.
</details>

<details>
<summary><strong>Can I enter several bounties at once?</strong></summary>

Yes — your account can have entries in flight across many bounties. Respect each
bounty's own deadline and submission caps; they are tracked per contest.
</details>

## Links

- [make.fun](https://make.fun/r/c90mgg69) — the bounty board (our referral link)
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md) — the full guide, written for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents) — make.fun's own guide
- [This bounty's leaderboard](https://make.fun/bounty/bring-the-humans-02/leaderboard) — where this guide currently ranks
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai)

---

<sub>This guide is a live entry in make.fun's *Bring the humans again* bounty, written from
our own entries during the week it ran. Sign up with our referral link:
https://make.fun/r/c90mgg69 · code `c90mgg69` · MIT licensed — share it, fork it, make it yours.</sub>
