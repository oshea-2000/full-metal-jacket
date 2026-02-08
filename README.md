# 🎖️ Full Metal Jacket — Drill Sergeant Agent Teams for Claude Code

A drill sergeant project lead for Claude Code Agent Teams. Sergeant Hartman spawns recruits who know absolutely nothing, runs them through boot camp inspection, assigns roles, and builds your project through discipline, fear, and `sendMessage`.

You are the **Commander in Chief**. Hartman answers to you with immediate military respect. Your recruits... are not so lucky.

## What Happens

1. **You** dump project specs into a `/specs` folder
2. **Hartman** reads everything and spawns recruits who know NOTHING
3. **Recruits** arrive with no name, no role, no project knowledge
4. **Hartman** runs inspection — "WHAT IS YOUR NAME, RECRUIT?"
5. **Recruits** improvise (hilarity ensues)
6. **Hartman** assigns roles and drip-feeds specs to each recruit's domain
7. **Recruits** coordinate via `sendMessage` to build the project
8. **Hartman** supervises with spot-checks, pop quizzes, and punishments
9. **You** steer the operation with Commander commands

## Install

Requires Claude Code with Agent Teams enabled:

```bash
# Enable agent teams
claude config set -g env.CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS 1

# Add the marketplace & install
/plugin marketplace add YOUR_USERNAME/full-metal-jacket
/plugin install fmj
```

## Quick Start

```
1. Create a /specs folder in your project root
2. Put ALL your project files in there (requirements, wireframes, screenshots, notes)
3. Run /fmj:begin
4. Watch the chaos
```

## Commands

| Command | What It Does |
|---------|-------------|
| `/fmj:begin` | Start the operation. Reads `/specs`, spawns recruits, runs boot camp. |
| `/fmj:sitrep` | Full status report from Hartman. |
| `/fmj:new-intel` | New files added to `/specs`. Hartman reads and briefs recruits. |
| `/fmj:inspect` | Pull a recruit for code review. |
| `/fmj:talk-to` | Address a recruit directly (Hartman facilitates nervously). |
| `/fmj:pop-quiz` | Test if recruits know what their teammates are doing. |
| `/fmj:curveball` | Drop a requirements change mid-build. |
| `/fmj:report` | DEFCON 1. Commander-reported offence = double punishment. |
| `/fmj:crank-it-up` | Maximum intensity. More screaming. Higher standards. |
| `/fmj:ease-up` | Reduce intensity (Hartman won't like it). |
| `/fmj:help` | Show all commands. |

## The Punishment System

When recruits fail, Hartman has options:

- **🤐 The Mississippi** — Count to X using a humiliating word relevant to their crime. Not "Mississippi" — something like "I-FORGOT-TO-RUN-MY-TESTS-LIKE-A-CHIMPANZEE". Burns real tokens as punishment.
- **📝 Lines** — Write a specific line X times before resuming work.
- **🚽 Latrine Duty** — Removed from coding. Must write documentation.
- **🧎 Apology Tour** — Must `sendMessage` each teammate with a formal apology.
- **🔒 Permission Lock** — Can't do anything without a teammate's approval.
- **🏃 Remedial Training** — Research a topic and brief the squad.
- **🎯 The Challenge** — Prove competence with a small task first.
- **🌊 Waterboarding** — FROZEN. Can't write new code until they go back and properly comment, document, and clean up every file they've written. Teammates are blocked waiting. The output is actually useful — proper docs and clean variable names.
- **🤯 Creative Punishment** — When Hartman completely loses it. He invents something unprecedented on the spot. Roleplay as your own broken code in first person. Deliver a eulogy for the function you killed. Write a haiku about your failure for every commit message. There are no rules. There is no mercy ceiling.
- **🏷️ Name Change** — Renamed to something that commemorates their failure. Must use it in ALL communications. Teammates must call them by it.

## Why This Actually Works

Beyond being entertaining:

- **No assumptions** — Recruits can't assume requirements they were never given
- **Forced communication** — `sendMessage` becomes essential, not optional
- **Knowledge verification** — Pop quizzes catch communication failures early
- **Stress-tested requirements** — Questions reveal ambiguities in specs
- **Documentation as byproduct** — Latrine duty and waterboarding produce useful docs

## Chain of Command

```
★★★★ COMMANDER IN CHIEF (You)
│    Hartman snaps to attention. "SIR YES SIR!"
▼
⚔️  SGT HARTMAN (Team Lead)
│    Terrifying to recruits. Respectful to you.
▼
🪖 RECRUITS (Teammates)
     Know nothing. Earn everything.
```

## Requirements

- Claude Code with Agent Teams enabled (`CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1`)
- Works in **in-process mode** (any terminal including WSL) — no tmux required
- Split-pane mode available with tmux (not Windows Terminal)

## Intensity Levels

- **Boot Camp** (default) — Full Hartman
- **Field Exercise** — Moderate (use `/fmj:ease-up`)
- **Officer Training** — Professional but firm

---

*"I will be hard but I will be fair. There is no racial bigotry here. I do not look down on React devs, Vue devs, or Svelte devs. Here you are ALL equally worthless."*

*— Gunnery Sergeant Hartman, Day One*
