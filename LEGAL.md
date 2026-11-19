# Safe harbor

This file quotes eero's published safe harbor. It is not legal advice. The live page controls:

https://hackerone.com/eero

**Fetched:** 18 November 2026 (America/Chicago) / 19 November 2026, 01:26 UTC. The policy overview was marked last updated 25 November 2025.

The program's Responsible Research and Disclosure section also says researchers must not access or collect customer data, must not exploit a vulnerability for any purpose other than testing, and must not publicly disclose the reported issue. Accidental exposure has to be reported, with written confirmation that the data was deleted. The policy says issues disclosed publicly or to a third party without consent may be ineligible for a reward.

## Quoted safe harbor

The following is the safe-harbor text from the program page, as fetched on the date above.

> Amazon will not bring any legal action against anyone who makes a good faith effort to comply with program policies, or for any accidental or good faith violation of this policy. This includes any claim under the Digital Millennium Copyright Act (DMCA) for circumventing technological measures to protect the services and applications eligible under this policy.
>
> As long as you comply with this policy:
>
> - We consider your security research to be "authorized" under the Computer Fraud and Abuse Act.
> - We waive any restrictions in our applicable Terms of Service and Acceptable Use Policy that would prohibit your participation in this policy, for the limited purpose of your security research under this policy.
>
> Amazon cannot authorize any activity on third-party products or technology (including any third-party technology that is included in, or that interoperates with, Amazon products) or guarantee that third parties won’t pursue legal action against you. We aren’t responsible for your liability from actions performed on third parties or their technology.

Two short bullets, about sharing PII with third parties and about sharing HackerOne points or participation, appeared after that section in the page extract without a heading. They are not copied here, because the extract did not show what they belonged to. Read them on the live page.

## What this does not cover

The quoted text limits authorization to research that complies with the policy, on the services and applications the policy covers. The same text says Amazon cannot authorize work on third-party products or technology. [SCOPE.md](SCOPE.md) records the program's separate exclusions for third-party systems and for direct attacks on AWS infrastructure.

Good-faith compliance includes the rules of engagement on the program page: accounts you own, the required User-Agent, the scanner rate limit, no customer-impacting denial of service, no social engineering, no physical attacks, no post-exploitation, and no public disclosure. Those rules are summarized in [SCOPE.md](SCOPE.md). Safe harbor is not a reason to skip them.
