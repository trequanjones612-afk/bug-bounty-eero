# Week 1 checklist

> **Re-read https://hackerone.com/eero on the day you start, and again before any request leaves a machine you own.**
>
> [SCOPE.md](SCOPE.md) is a snapshot from 18 November 2026 (America/Chicago). The live policy wins if they differ.
>
> This checklist is planning. It names work and bug classes. It does not describe how to break anything. No testing begins until the Day 1–2 items are done, and no testing goes outside the live rules.

Prefer a **spare eero you own, on its own network**, so the household mesh is left untouched. If there is no spare node, pause device work. Do not experiment on a network other people are using.

## Ground rules

- Accounts and devices you own, only.
- No denial of service, no brute force, and no other availability testing. The program forbids customer-impacting denial of service, and it forfeits a reward for application-level availability tests that skip its cache-buster and self-hosting conditions. Week 1 does not run those tests at all.
- No social engineering, phishing, or physical attacks. No support chats. No employees. No customers.
- No post-exploitation and no pivoting.
- Scanners only inside the published limit: the User-Agent `eeroResearcher_<h1username>`, and no more than 5 requests per second to any one service.
- No third-party XSS-hunter sites. Traffic stays on infrastructure you own and control.
- Stop at the first sign of another person's data. Report it, delete it, and do not keep a copy.
- One spare research node. The household mesh stays out of scope for this week.
- Notes that describe a real result go in `notes/private/` (gitignored) or straight into a HackerOne draft. They do not get committed while this repository is public.

## Order of work

1. Setup, inventory of hardware you own, and a firmware check against the latest offered software.
2. Two eero accounts you own, both on HackerOne aliases. The class to think about is broken access control, including IDOR, between those two accounts.
3. The official Android app (`com.eero.android`), on those same accounts. The class to think about is session handling.
4. A light inventory of local services on the spare research node only.
5. Optional offline notes later, in `notes/private/`, after the week. Not in git.

## Day 1–2 — setup, inventory, firmware

- [ ] Create a HackerOne account, if you do not already have one, and join the eero program at https://hackerone.com/eero.
- [ ] Confirm past-year Signal. The page requires 0.0 or higher and says hackers below that use trial reports.
- [ ] Read the full policy, including the non-qualifying lists and [HackerOne's core ineligible findings](https://docs.hackerone.com/en/articles/8494488-core-ineligible-findings).
- [ ] Record the researcher identity you will use. The program says to create eero accounts as `<h1username>@wearehackerone.com`. Put your HackerOne username into the User-Agent `eeroResearcher_<h1username>` before any testing traffic.
- [ ] Inventory eeros you own: model, nickname, where it sits, and whether it is the spare research node or part of the household mesh. Household nodes are listed so they can be avoided.
- [ ] Confirm each candidate research device is on the [security-updates table](https://support.eero.com/hc/en-us/articles/4401964665243-eero-Software-Security-Updates) with a support date that is not in the past. A first-generation (2016) eero is not in the table fetched on 18 November 2026 and does not meet that test. See [SCOPE.md](SCOPE.md).
- [ ] In the eero app, tap the node's nickname, then Software updates, and write down the installed version and whether an update is offered. Public release notes on the fetch date listed eeroOS **v7.18.0** (12 November 2026) as the newest version, and they say rollout takes weeks. "Latest" means the latest software offered to that device, checked in the app, not a version copied from this file.
- [ ] Write down the installed version of the official Android app. The in-scope package on the policy page is `com.eero.android`.
- [ ] Copy the in-scope domain wildcards from the live scope table (`*.eero.com` and `*.e2ro.com` at the time of the snapshot) and remember the WHOIS check before any report about a hostname. Do not build a scan list in this repository.

## Day 3–4 — two accounts you own

Class: **broken access control / IDOR between two accounts you control.** The question is whether one account you own can read or change the other account you own. Impact stays on your own resources.

- [ ] Open two eero accounts you own. The program's required address is `<h1username>@wearehackerone.com`. A second account can use a plus-alias, `<h1username>+<label>@wearehackerone.com`, which [HackerOne's alias article](https://docs.hackerone.com/en/articles/8524970-hacker-email-alias) says forwards to the same hacker. The eero policy does not mention plus-aliases. If signup rejects one, stop and do not use an address you do not own.
- [ ] Keep a private note of which alias is which account. Do not commit the addresses with any token, reset link, or mailbox dump.
- [ ] Think about authorization between those two accounts only. Do not open, guess, or test an account that is not yours.
- [ ] If something looks like a real cross-account issue, stop testing and move to the Day 7 report path. Do not keep pulling data to see how far it goes.

## Day 5 — official Android app

Class: **session handling on the official app**, for accounts you own. The question is whether a session stays attached to the account you signed in, and whether it ends when you log out. No token theft, no instrumentation notes, and no modified client in this repository.

- [ ] Sign in and out of each of your two accounts on the phone you own.
- [ ] Note the app version and the eeroOS version the app shows for the spare node.
- [ ] Stay on `com.eero.android` from the official store. The iOS app id on the policy is `1023499075`, for a later week if you own an Apple device. Do not add a second client this week.

## Day 6 — spare node, light inventory

Activity: **inventory of local services on the one spare research node**, at the level of "what does my own node offer on my own network." Write the list in `notes/private/` if it is specific. A committed note may name the class ("local services on a node I own") and nothing finer.

Related class, still names only: **device update integrity** — whether that node installs the software eero published. Confirming the version in the app is the whole of this item. No firmware dumping, no image unpacking, no signature work.

- [ ] Confirm again that this node is the spare, not a household node.
- [ ] Confirm the app still shows the latest offered software.
- [ ] List, privately, the services that node presents to your own LAN. Stop at the inventory. No follow-up requests aimed at breaking a service.
- [ ] Optional, later: deepen that private inventory, or pause. Either one is a complete week if no reportable issue showed up.

## Day 7 — report, or stop

- [ ] If you have a candidate that fits the live policy, is not on the non-qualifying list, and affects only resources you own: fill [reports/TEMPLATE.md](reports/TEMPLATE.md) **locally and privately**, then submit through HackerOne. Do not commit the filled report. One root cause per report.
- [ ] If you do not: either extend the same high-level inventory, or pause. Do not widen onto the household mesh, third-party hosts, or AWS to fill the day.

## Classes for the week

Names only. A class is a thing to keep in mind while you look at your own accounts and your own spare node. Nothing below is a procedure.

| Class | What the question is | Where it lives |
| --- | --- | --- |
| Broken access control, including IDOR | Can account A, which you own, read or change account B, which you own? | Days 3–4 |
| Mobile session handling | Does the official Android app keep a session tied to the account you signed in, and drop it when you log out? | Day 5 |
| Device update integrity | Is the spare node running the software eero offered, as shown in the app? | Days 1–2 and 6 |
| Local service inventory | What does the spare node present on your own network? Inventory only. | Day 6 |
