# eero HackerOne research notebook

This repository is a planning notebook for **authorized** research under eero's published bug bounty program on HackerOne:

https://hackerone.com/eero

It is not a GitHub Security Bug Bounty notebook. The only program these notes follow is the eero program at the link above.

**Re-read the live policy before any testing.** This repository is a snapshot and a checklist. The page on HackerOne is the policy. If a note here and the live page disagree, the live page wins.

Pages were read on **18 November 2026 (America/Chicago)** / **19 November 2026, 01:26 UTC**. Policy text on the program page was marked last updated **25 November 2025**. The rewards table on that page was marked last updated **11 November 2025**.

## This repository is public

**The GitHub repository is public.** Make it private before storing any note that could describe a real finding.

Do not commit credentials, tokens, session cookies, captures, firmware dumps, screenshots that show personal data, or another person's data. A private report belongs on HackerOne, and only there, while the issue is unfixed.

`reports/` is gitignored except `reports/TEMPLATE.md`. `notes/private/` is gitignored. Those ignores are a backstop. They do not make a public repository a safe place for a live finding.

## Purpose

Track scope, rules, and week-by-week planning for research on accounts and devices the researcher owns, inside the rules eero published. Success for this notebook is a clear record of those rules and an empty place to plan. It is not a place to develop or store attack material.

## How we work

- Use only accounts and devices you own.
- Create eero accounts with the HackerOne address the program requires, and send the User-Agent the program requires. Both are copied in [SCOPE.md](SCOPE.md).
- Keep scanners inside the rate limit stated on the program page, and only with that User-Agent.
- Stop when research touches another person's data. Report what was accessed, delete it, and do not keep a copy.
- Submit through HackerOne only. Do not publish an unfixed issue in this repository, in a fork, or anywhere else.
- Prefer a spare eero you own, on its own network, so the household mesh stays untouched. See [WEEK1.md](WEEK1.md).

## Map

| Path | What it is |
| --- | --- |
| [SCOPE.md](SCOPE.md) | Snapshot of scope, rewards, and rules from the live program page |
| [WEEK1.md](WEEK1.md) | First-week checklist inside those rules |
| [LEGAL.md](LEGAL.md) | The program's safe-harbor language, quoted and linked |
| [reports/TEMPLATE.md](reports/TEMPLATE.md) | Empty outline for a private HackerOne report |
| [notes/](notes/README.md) | Working notes. Live finding details do not belong in a public repo |

## What does not belong in this repository

Exploit code, proof-of-concept code, payloads, attack scripts, packet recipes, firmware reverse-engineering notes, and step-by-step reproduction of a vulnerability. Name a bug class in a checklist if you need to. Leave the method out.
