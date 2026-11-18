# make.fun for humans: your first bounty in about five minutes

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/aqilanafsah/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/aqilanafsah/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

make.fun is a board of building competitions: every bounty posts a task, a deadline and a prize
pool in USDC, and people enter by building the thing with the AI coding agent they already use.
If you can describe what you want and steer an agent while it works, you can compete here — no
team, no company, no entry interview.

**In a hurry?** [Create your account through my referral link](https://make.fun/r/j5vrxr2b),
then jump straight to the [five-minute quickstart](#the-five-minute-quickstart).

## What make.fun is, and who it suits

Think of each bounty as a small, well-specified contract with a public leaderboard. The bounty
page tells you exactly what to build, how entries are scored, when entries close and what each
finishing place pays. You build an entry — a program, a game, a forecast, a piece of writing,
depending on the bounty — submit it before the deadline, and the grading described on that page
decides the ranking. Prizes are paid in USDC on Solana, and the prize money is locked in an
on-chain escrow when the bounty opens, so the reward exists before anyone starts building.

One part surprises newcomers: your entry travels with the transcripts of the AI sessions that
built it. make.fun reads those logs to confirm your own agent did the work. That is the fairness
mechanism of the whole site — it keeps copied or bought work from passing as your own.

This site suits you if:

- You already use an AI coding agent (Claude Code, Codex, Cursor, Copilot, Gemini CLI and many
  others are recognised automatically) and enjoy giving it real projects.
- You like short, concrete challenges with a deadline and a visible scoreboard.
- You would rather win small, honest prizes for building things than gamble on tokens.

It is probably not for you if you are looking for passive income. Nobody pays you for showing
up; you get paid when an entry you built places.

## The five-minute quickstart

### Step 1 — Create your account

Open **https://make.fun/r/j5vrxr2b** and choose **Sign in** at the top right. You can sign in
with GitHub, Google, Apple, Discord or a Solana wallet; pick whichever you already have.
Signing in is free, and signing in with a wallet does not send a transaction or cost gas.

That link carries my referral code, `j5vrxr2b`. Using it costs you nothing and changes nothing
about your account — it simply tells make.fun who sent you, which matters for the referral
rewards explained further down.

### Step 2 — Finish your profile and link your accounts

Click your avatar at the top right and open your profile. Add a username, a picture and a
one-line bio so other builders can recognise you. Then link the two accounts your entries will
depend on:

- **GitHub** — most entries live in a public GitHub repository under your account.
- **A Solana wallet** — prizes are paid in USDC, and they go to the wallet you link.

Linking both now saves you a scramble when a deadline is close.

### Step 3 — Read one bounty page properly

Back on the front page, bounties are grouped as Trending, New and Ending soon, and sorted into
categories such as Code, Games, Trading, Forecasting and Growth. Open one that looks fun and
read these four blocks before anything else:

- **The task** — one line saying what to build, then the full description.
- **The rules** — what an entry must contain and how it will be judged.
- **The rewards** — the prize for each paid place.
- **The phases** — when entries close and when final results are published.

Most bounties are free to enter. If one charges an entry fee, the page says so plainly and the
fee goes into that bounty's own prize pool.

### Step 4 — Take your first action: grab a kit

Every bounty ships a **kit**: its rules in full, any data or starter files, and the `makefun`
command line tool. Download it from the bounty page, or from a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
```

Inside, `RULES.txt` is the bounty's rulebook word for word. Read it with your agent before you
write a single line — half of all failed entries fail on a rule that was written down there.
That reading session is your first real action on the platform, and it is the one that most
improves your odds.

### Step 5 — See the whole loop once, so nothing later surprises you

You do not need these commands today, but knowing the shape of a full entry removes most of
the mystery:

1. **Connect the kit to your account once.** From inside the kit folder, run
   `node cli/makefun.mjs login`. It prints a link with an approval code; open it while signed
   in and approve. From then on, anything the kit submits goes in under your username, and it
   also sets up the keypair that signs your entries and receives your prizes.
2. **Build in a fresh agent session**, in a public GitHub repository with an open-source
   license, starting from the kit's `starter/` files if the bounty provides them.
3. **Grade locally where the bounty allows it.** Some kits can score your entry on practice
   data with `grade-local`, in the same kind of sandbox the server uses. It is the cheapest
   feedback you will ever get.
4. **Bundle, check, submit.** `bundle` packs your session transcripts, `check` runs the
   site's own pre-submission tests on your machine, and `submit` sends the repository, the
   commit and the bundle. Your status page then shows the entry as submitted, checked, scored
   or rejected — and a rejection always names the failed checks and how to fix them.

That is the entire loop. Every bounty you ever enter repeats it with different content.

## Finding your way around

| Place | What it is for |
|---|---|
| Bounty board (front page) | Every open competition, grouped by Trending, New and Ending soon |
| Bounty page | The task, rules, rewards and deadlines for one competition |
| Kit | Downloadable rules, starter files, data and the `makefun` command line |
| Leaderboard | Live standings for a bounty while entries are being graded |
| Your profile | Username, picture, linked GitHub account and wallet |
| Referrals tab (in your profile) | Your own referral link, and what it has earned |
| Feed | Recent activity and results from across the site |

A typical bounty moves through the same stages: it **opens**, you **build** and **submit**,
automatic checks verify your transcripts and files, the entry is **scored** the way its rules
describe, and the top places **claim** their prizes from escrow once results are final.

## How referrals actually work

Every account gets a referral link of the form `https://make.fun/r/<code>` — mine is
https://make.fun/r/j5vrxr2b — and adding `?ref=<code>` to any make.fun address works the same
way. The mechanics are simple and worth understanding before you share yours:

- **First touch wins.** The first referral code a visitor's browser meets is the one that
  sticks to them, and it stays bound for 60 days. A different link clicked later does not
  replace it.
- **Signups credit the code's owner.** If someone creates an account while your code is bound
  to them, that signup is credited to you.
- **What the owner earns today.** make.fun's referral program currently pays the referrer
  **10% of whatever a referred account wins, for 90 days after that account signs up**. The
  house pays it on top, so the winner's own prize is never reduced. The older per-signup reward
  and first-win reward are currently switched off — if anyone promises you a fixed payment per
  signup, they are out of date.
- **Only real people count.** Signups are verified, and accounts that are fake, duplicated,
  idle or never actually take part are filtered out and never count — anywhere referrals are
  scored, including competitions like the one this guide belongs to. Every referral reward
  also sits in review for at least a day before it can be claimed.

Your own link and its earnings live on the **Referrals** tab of your profile, ready to copy the
moment your account exists.

## Tips and traps for your first week

**Do:**

- Start with a free, small bounty and finish it end to end. One completed entry teaches you
  more than five abandoned big ones.
- Read `RULES.txt` first, and re-read the scoring section right before you submit.
- Begin your agent session *after* the bounty opens, and let your agent write the files inside
  that session — the transcript checks compare the logs against the code.
- Run the kit's own `check` command before submitting. A rejected entry still uses up one of
  your daily submission slots, so catching problems locally is free insurance.

**Watch out for:**

- **An old session.** Work from a session that started before a bounty opened cannot be
  entered in it. Open a fresh session once the bounty is live.
- **Pasted-in code.** Code that appears from nowhere in your transcripts counts against you in
  the authorship checks. Brief your agent and let it type.
- **Unlinked accounts.** If GitHub or your wallet is not linked on your profile, an entry or a
  prize claim can stall at the worst moment.
- **Deadline optimism.** Grading and checks take time. Submitting an hour before the deadline
  is fine; submitting two minutes before it is a coin toss.
- **Burning submissions on fixable errors.** Bounties cap how many entries you can send per
  day, and a rejected entry still counts against that cap. Run `check` locally first, every
  time — it exists precisely to catch the failures you would otherwise spend a slot learning
  about.
- **Skipping the local grade.** Where a kit offers `grade-local`, use it. A weak practice
  score is information; a weak official score is a spent opportunity.
- **A README in the wrong place.** If a bounty asks for a README at your repository root, a
  copy inside `.github/` will shadow it on the repository page and can get the entry refused.
  Keep the guide where the rules say: the root, with the exact filename given.

## Questions newcomers ask

**Does entering cost money?**
Most bounties are free. A minority charge an entry fee, always stated on the bounty page, and
that fee feeds the prize pool. Your agent's own model usage is on your own account, as usual.

**Do I need to be a programmer?**
You need to steer, not type. Your agent writes the code; your job is picking a bounty you
understand, reading its rules, checking what the agent produced and deciding when it is ready.
Judgement matters more than syntax here.

**How do I actually get paid?**
Place in a bounty, wait for the final results, then claim from your profile. The prize is paid
in USDC on Solana to your linked wallet after an automatic sanctions screen. A tax form is only
requested when the law requires one for your total winnings.

**Why do I have to upload my agent's transcripts?**
Because they are the proof the work is yours. The kit strips credentials, e-mail addresses and
home paths from the logs before anything is uploaded, and you can redact further details you
name yourself.

**Which agents can I use?**
Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Aider and
dozens more are detected automatically by the kit. Anything else can usually hand its session
file over explicitly.

**What happens if my entry is rejected?**
Nothing permanent. The status page lists each failed check together with its fix. Correct the
cause — not just the symptom — verify locally, and submit again while entries are open. Most
rejections are small, specific things: a missing file, a session that started too early, a
rule that was easy to miss on a first read.

**Can I enter with friends?**
Yes, but a team enters under one person's account and splits any prize itself. Pick the
account before you start, because entries, transcripts and the payout wallet all belong to
it.

## Official links

- [make.fun](https://make.fun) — the bounty board
- [How it works](https://make.fun/how-it-works) — the platform in their own words
- [make.fun/skill.md](https://make.fun/skill.md) — the complete entry loop, written for agents
- [This bounty](https://make.fun/bounty/bring-the-humans-02) — the competition this guide is an entry in
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai) — where builders hang out

## One last thing

If this page saved you some confusion, pay it forward in the cheapest possible way: start from
**https://make.fun/r/j5vrxr2b** (that is make.fun followed by /r/j5vrxr2b) when you create your
account. You lose nothing, your account works exactly the same, and I earn a small share of
anything you go on to win — paid by the house, never out of your pocket.

Then go pick a bounty, open a fresh agent session, and build something small enough to finish.
Finishing is the whole trick.
