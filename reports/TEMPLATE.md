# Report template

Copy this file locally. Do not fill it in on the public branch, and do not commit the copy.

Submit the finished report through HackerOne only: https://hackerone.com/eero

One root cause per report. A minimal proof of concept, if you need one, runs only on accounts and devices you own, and it travels only in the HackerOne report. While the issue is unfixed, it is not published here, in a fork, or anywhere else.

Re-read the live policy before you submit. Reward, severity, and eligibility are Amazon's decision. The ranges in [SCOPE.md](SCOPE.md) are the published maxima, not a quote.

If this report is a bypass of one of your own earlier reports, put the original report ID in the HackerOne custom field `Bypass Reference`. The policy says that field is for tracking and does not change the reward.

---

## Title

[One sentence. Name the component you own and the impact on your own resources. No exploit detail in a committed file.]

## Severity guess

- Guess: [Low / Medium / High / Critical]
- Asset band: [Services, Apps, Mobile / Devices]
- Why this band, in one or two sentences, using only the impact on resources you own: [Placeholder]
- CVSS 3.0 vector, if you have one: [Placeholder. The program says HackerOne uses CVSS 3.0 and that Amazon may score lower because of compensating controls.]

## Impact

[What a holder of your own account, or a party on your own device, can do that they should not. Stay on your accounts and your devices.]

## Affected product

- Software version (required by the program): [Placeholder]
- Device model, if any: [Placeholder]
- App and version, if any: [Placeholder. Android package on the policy: `com.eero.android`. iOS app id on the policy: `1023499075`.]
- Account identifiers you own (HackerOne aliases only, no passwords or tokens): [Placeholder]

## Steps to reproduce

Placeholder sections only. Write the real steps in the private HackerOne report.

1. [What you did, on an account or device you own.]
2. [What you did next, still on resources you own.]
3. [What you observed.]

## Proof of concept

[Placeholder. Minimal demonstration on resources you own. Paste it only in the HackerOne report. Do not paste it into this repository.]

## Accounts and devices used

- Account A: [alias you own]
- Account B, if any: [alias you own]
- Phone: [your device, app version]
- eero: [your spare research node, model, eeroOS version shown in the app]
- Household mesh was not part of the test: [yes / no]

## Timestamps

- First observed (timezone): [Placeholder]
- Last confirmed (timezone): [Placeholder]

## Other people's data

- Encountered: [no / yes]
- If yes: testing stopped, the program was told what was accessed, and the data was deleted. Nothing from that data is in this report beyond what the program needs to investigate.

## Remediation suggestion

[Optional. The change that would remove this single root cause. No exploit detail.]

## Out of scope for this report

[Anything you saw and did not chase. One root cause only.]
