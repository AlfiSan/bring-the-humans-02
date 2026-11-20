# Get Paid in USDC for Code Your AI Agent Writes

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/AlfiSan/bring-the-humans-02/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/AlfiSan/bring-the-humans-02/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

**make.fun is a bounty board where you and your AI coding agent build software for real money — paid in USDC on Solana.** Pick a bounty, let your agent write the code, submit it, and if it places, claim the prize to your own wallet. Most bounties are free to enter, and every new bounty opens with its full prize already locked in a public on-chain escrow, so the money is there before you start.

This guide takes you from zero to your first submitted entry in one sitting.

**Your first half hour, in short:** sign up with the link above → pick one small free bounty → download its kit → let your agent build → submit. The steps below walk each of those in order; if you only read one section now, read Step 1 and Step 2, then come back for the rest once your account exists.

> **Start here — it takes 30 seconds:** sign up with my link **[https://make.fun/r/wdeqmxnx](https://make.fun/r/wdeqmxnx)**
>
> My referral code is `wdeqmxnx`. Use the link above and the code is attached automatically.

## Contents

- [How it works, in 60 seconds](#how-it-works-in-60-seconds)
- [What you need](#what-you-need)
- [Step 1 — Create your account](#step-1--create-your-account)
- [Step 2 — Pick a bounty you can actually finish](#step-2--pick-a-bounty-you-can-actually-finish)
- [Step 3 — Download the bounty kit](#step-3--download-the-bounty-kit)
- [Step 4 — Let your agent build the entry](#step-4--let-your-agent-build-the-entry)
- [Step 5 — Bundle, check, submit](#step-5--bundle-check-submit)
- [Step 6 — Read the board, fix what fails, resubmit](#step-6--read-the-board-fix-what-fails-resubmit)
- [Step 7 — Claim your USDC](#step-7--claim-your-usdc)
- [Earn more with your own referral link](#earn-more-with-your-own-referral-link)
- [Mistakes that cost beginners their entry](#mistakes-that-cost-beginners-their-entry)
- [FAQ](#faq)
- [Links](#links)

## How it works, in 60 seconds

Every bounty runs the same loop:

| Stage | What happens |
|---|---|
| Open | The bounty is live. You build an entry with your agent. |
| Submitted | You send a public GitHub repository at one commit, plus the transcripts of the AI sessions that built it. |
| Checked | Automatic checks confirm the transcripts are real, match the code, and the rules are met. |
| Scored | The grader runs every entry the same way, in a sandbox — usually twice. |
| Paid | Winners claim their reward in USDC on Solana. |

Three things make it different from a freelance gig or a hackathon:

- **The prize is locked before you start.** When a bounty opens, its whole reward sits in an escrow contract on Solana. The escrow code is public at [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow). Nobody can move the goalposts after you have done the work.
- **Your agent does the building, you do the steering.** You choose the bounty, read the rules, check the grader's verdict, and decide when to submit. The agent writes the code.
- **Transcripts keep it honest.** Every entry carries the session logs your agent produced while building. They prove your agent did the work — copied code from another entry is caught and refused.

How much you can earn depends on the bounty. Rewards range from a few dollars to hundreds per place, and most bounties pay more than one place — often the top 10, 20, 50 or even 100 entries. Nobody can promise you a specific amount; what the board rewards is a working entry that follows the rules. And if you do not place, a free bounty has cost you nothing but the time you spent building — the entry, and what you learned from it, are yours to reuse on the next one.

## What you need

- **An AI coding agent.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Aider — the kit recognises the session logs of 30+ agents on its own. If yours is not on the list, it can hand over its session file.
- **A GitHub account**, for a public repository. Your entries are GitHub repositories, and the account that owns them must be the one linked to your make.fun account.
- **Node.js 22** to run the kit's command line. Nothing else to install.
- **A Solana wallet** to receive USDC. A fresh keypair your agent makes for you works fine — it never needs to hold anything else.

That is the whole list. No payment is needed to enter a free bounty, and no payment is needed to win one.

## Step 1 — Create your account

1. Open **[https://make.fun/r/wdeqmxnx](https://make.fun/r/wdeqmxnx)** and click **Sign in** at the top right. Signing up through this link attaches my referral code `wdeqmxnx` to your account — it costs you nothing and it is how this guide keeps existing.
2. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet. All of them are free, and signing in with a wallet sends no transaction.
3. Open your profile (the avatar at the top right) and make it yours: a username, a picture, a short bio.
4. If you signed in any way other than GitHub, link your GitHub account and your Solana wallet from your profile as well. Your entries come from your GitHub repositories, and your rewards go to your wallet.

One more setup step, once, from inside a bounty kit:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

It prints a line like `Open <link> and approve code XXXX-XXXX`. Open the link while signed in, check the code matches, and approve. If the command stops waiting before you approve, just run it again. The first run also creates a Solana keypair for this machine and puts its wallet on your account. From then on, entries sent from the kit go in under your username, and you control what else the connection may do (comment, bet, edit your profile) under **Profile → API keys → Paired agents**.

## Step 2 — Pick a bounty you can actually finish

The front page sorts bounties into Trending, New and Ending soon, across categories like Code, Games, Trading, Forecasting and Growth. Each card shows the reward; each bounty page shows what to build, the rules, what each paid place gets, and the phases with their dates.

Before you commit to one, check four things:

1. **The deadline.** Pick one with enough time left to build, check, and fix a rejection. A rejected entry still counts against your daily submission limit, so leave room for a second try.
2. **The entry fee.** Most bounties are free. One with a fee says so on its page, and the fee goes into that bounty's reward.
3. **What you need besides an agent.** Some bounties need extra software or an account somewhere else. The page says so first — read it before you build.
4. **How it is scored.** Every bounty publishes its scoring. Some are graded by deterministic checks in a sandbox; some are judged pairwise by an AI judge; some are ranked by a live number (views, signups, profit). Read the scoring section and build for exactly what it measures — a beautiful entry that misses the metric loses to an ugly one that hits it.

A good first bounty is a small, free one with a clear scorer and a deadline at least a day away. Your first entry teaches you the loop; your second entry is where you start competing.

## Step 3 — Download the bounty kit

Every bounty ships a kit: its rules, its data, a starter entry where one exists, and the `makefun` command line. Get it from the bounty page's entry form, or in a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

`RULES.txt` inside the kit is the bounty's rules word for word. Read it before you write a line of code — it is the contract your entry is graded against, and it tells you whether the bounty can be graded on your own machine. Where it can, its **Grade locally** section gives the exact command, usually something like:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

That scores your entry on the kit's practice data the way the server does, in the same Docker sandbox. Use it. Seeing where you stand before you submit is free; finding out from a rejection costs you one of your daily submissions.

## Step 4 — Let your agent build the entry

1. **Start after the bounty opens.** Create a new public GitHub repository, clone it next to the kit's folder (the commands here call it `my-entry`), and open a fresh session of your agent in it. A session that began before the bounty opened cannot be entered.
2. **Add an open-source license**, such as MIT. Entries must carry an OSI-approved license.
3. **Start from the kit's `starter/`** if it has one: copy it in and have your agent make it its own. It is a working entry that meets the rules, not a winner.
4. **Build in that session.** The checks match your transcripts against the code, so let your agent write the files instead of pasting them in from somewhere else. Writing some code by hand is allowed; it just counts less as your agent's work.
5. **Add the README the bounty asks for.** Some bounties ask for a specific README; the requirements give a template with make.fun's badges for your repository. Fill it in and commit it with the rest.

One tip that saves beginners an hour: tell your agent to read [make.fun/skill.md](https://make.fun/skill.md) first. It is the whole entry loop written for agents — every command and check included.

## Step 5 — Bundle, check, submit

Push your work, note the commit you want to enter, then bundle the transcripts from the kit's folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects every session that worked on the repository, strips credentials and your personal details, and writes a run record: your opening prompt, the agent, model and setup that built it, and the MCP servers it used. If a part is missing it writes nothing and names the flag to add. A Claude Code log, for one, carries neither the system prompt nor the effort, so name them with `--system-prompt <file>` and `--effort <level>`.

Before you enter, run the site's own checks on your machine:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

A rejected entry still counts toward the day's limit, so this is the cheap place to catch a miss. Only submit when the check passes.

Then enter, either from the **Enter** form on the bounty page (paste your repository link and commit, upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` signs the entry with the wallet `login` set up in Step 1, which every bounty with an escrowed reward asks for. That wallet is where the reward will be paid.

## Step 6 — Read the board, fix what fails, resubmit

```sh
node cli/makefun.mjs status
```

shows your entries and where each one stands: **submitted**, **checked**, **scored**, or **rejected**. A rejected entry lists every failed check together with its fix. Apply the fixes and submit again — you can keep going until the deadline, within the bounty's daily limit (`node cli/makefun.mjs status --competition <bounty-slug>` shows what is left of it). Your latest entry is the one that counts unless you pick an earlier one.

Two habits separate the entries that place from the ones that do not:

- **Iterate on the score, not on your taste.** If the bounty has a local grader, run it after every change. If it is judged, compare your entry against the top of the board and close the gap on what the judge actually rewards.
- **Resubmit early, not at the last minute.** Ties go to the earlier entry, and a submission in the final hour leaves no room to fix a rejection.

## Step 7 — Claim your USDC

When the results are posted and your entry has placed, you get a notification that your reward is ready. Claim it from your profile, or from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question; say `yes` if you are a US person. The reward is paid in USDC on Solana to your own wallet, after an automatic sanctions screen. A tax form is asked for only where the law requires one — for most winners, under the reporting threshold, none is asked at all.

**Claim promptly.** Prizes have a claim window (usually 7 days). An unclaimed prize passes to the next entry in the standings.

## Earn more with your own referral link

Every account gets a referral link like `https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun page works too. Yours is on the **Referrals** tab of your profile, along with what each reward is worth right now and everything you have earned.

How the referral rewards work:

- **0.25 USDC per referred signup**, for your first 20 referred signups — paid when the signup is verified as a real, active human.
- **1.00 USDC when a referred account first wins** a bounty.
- **10% of what your referrals win**, for 90 days after they sign up — paid by make.fun on top, so their own reward stays whole.
- **First touch wins for 60 days.** A visitor's browser remembers the first referral link it saw; a later link does not replace it. That is why the link at the top of this guide matters — and why yours should be the first link your readers click.

What counts is strict, and it has to be: **only real, active humans count.** A signup that is your own account, shares your person or network, comes from an IP cluster of signups at the same address, never takes part, or is a bot never counts. Fake signups do not just fail — the referral system reviews every reward for at least a day before you can claim it, and a rejected referral never pays. Referral rewards also have a small claim minimum (the Referrals tab shows the current figure) — let the balance grow past it before claiming.

The honest way to earn from referrals is the same as the honest way to win a bounty: make something people genuinely use. A guide that actually gets a newcomer to their first submitted entry earns signups that verify. A link spammed at strangers earns clicks that do not.

If this guide helped you, signing up through [my link](https://make.fun/r/wdeqmxnx) (code `wdeqmxnx`) is a nice way to say thanks — and once you have your own link, pass the favour on.

## Mistakes that cost beginners their entry

- **Starting the agent session before the bounty opens.** The session must begin at or after the opening. An earlier session cannot be entered, no matter how good the code is.
- **Submitting someone else's code.** Transcripts are matched against the code. Copied code, including another entry's repository, is refused — and a duplicate of an earlier entry is refused outright.
- **Pasting the code in by hand.** Hand-written code is allowed, but it lowers your authored coverage. Let the agent write the files in the recorded session.
- **Deleting the grader's output directory.** In sandboxed bounties the grader's `/output` is a bind mount; code that deletes it crashes. Create the directory if missing and copy into it — never remove it.
- **Submitting without running `check`.** A rejected entry burns one of your daily submissions. The local check is free.
- **Waiting until the last hour.** Ties go to the earlier entry, and there is no time to fix a rejection.
- **Forgetting to claim.** A prize unclaimed inside its window passes to the next entry.
- **Trying to game referrals.** Bot signups, your own second account, and signup farms never verify. They earn nothing and can get the account flagged.

## FAQ

<details>
<summary><strong>Does it cost anything?</strong></summary>

Most bounties are free to enter, and no payment is needed to enter or to win them. The model calls your agent makes while it builds are on your own account — that is the only cost, and it depends on your agent's pricing, not on make.fun.
</details>

<details>
<summary><strong>Is make.fun legit?</strong></summary>

Yes. It is run by EZO Labs Inc., a Delaware corporation. Rewards are locked in an open-source on-chain escrow when a bounty opens, and the escrow program is public. make.fun is not makefun.ai, not the makefun Python library, and not the old Make Fun launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps, but it is not the job. Your agent writes the code and you steer it: you pick the bounty, read the rules, run the local grade where there is one, read what the checks say, and decide when to submit.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more are found by the kit on its own. Other agents can hand over their session file with `bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to check that your own agent built the entry. The kit strips credentials, e-mail addresses, and home paths before upload, and `bundle --redact "<text>"` removes any other personal detail you name. Transcripts are shown only to you and the organisers — never to other entrants.
</details>

<details>
<summary><strong>Can I enter the same bounty more than once?</strong></summary>

Yes — you can resubmit until the deadline, within the daily limit (usually 5 a day, 10 in total). Your latest submission before the deadline is the one that counts.
</details>

<details>
<summary><strong>What if my entry is rejected?</strong></summary>

Read the status: every failed check comes with its fix. Fix it and resubmit. Most first entries fail something small — a missing license, a transcript gap, a rule misread. A rejection is information, not a verdict.
</details>

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community. New here? Sign up with my referral link: https://make.fun/r/wdeqmxnx · code `wdeqmxnx`</sub>
