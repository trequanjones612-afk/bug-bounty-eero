# eero program scope (snapshot)

> **Re-read the live policy before any testing.**
>
> https://hackerone.com/eero
>
> This file is a snapshot of that page and the firmware articles it points to. It is not permission to test, and it is not a substitute for the live page. If a line here is stale, the live page wins. Do not treat a third-party scope mirror as the policy.

**Fetched:** 18 November 2026 (America/Chicago) / 19 November 2026, 01:26 UTC.

**Primary source:** [eero program policy](https://hackerone.com/eero). The policy overview was marked last updated **25 November 2025**. The rewards summary was marked last updated **11 November 2025**.

**Also read:**

- [Structured scope table](https://hackerone.com/eero/policy_scopes) and [scope versions](https://hackerone.com/eero/scope_versions). A non-JavaScript fetch of the scope table returned only the HackerOne application shell, so the asset identifiers below are taken from that table's published rows as indexed on the fetch date. They match the policy prose and the "5 assets in scope" highlight. **TODO:** open the live table in a browser and correct this file if a row differs. Do not add hostnames from third-party scope mirrors.
- [eero Software Security Updates](https://support.eero.com/hc/en-us/articles/4401964665243-eero-Software-Security-Updates) (the firmware reference named on the program page).
- [eero Software Release Notes](https://eero.com/support/articles/eero-software-release-notes).
- [How do I check my eeroOS version?](https://www.eero.com/support/articles/how-do-i-check-my-eeroos-version).
- [HackerOne core ineligible findings](https://docs.hackerone.com/en/articles/8494488-core-ineligible-findings).
- [HackerOne email alias](https://docs.hackerone.com/en/articles/8524970-hacker-email-alias).
- [HackerOne platform standards](https://docs.hackerone.com/en/articles/8369826-detailed-platform-standards).

## Program highlights shown on the fetch date

These numbers change. They are not a promise.

The page presented the program as **closed scope** (only listed scope), with a **fast payment** highlight ("Ensures payment within 1 month of receiving a vulnerability report"), **collaboration enabled, including retesting**, and this signal rule: **0.0 or higher past-year Signal required, with use of trial reports for hackers below it.**

Response figures shown that day: about 3 days 3 hours to first response, 3 days 20 hours to triage, 3 weeks 4 days to bounty, 4 weeks 1 day from submission to bounty, and 2 months 1 week to resolution. Response efficiency was shown as 78%. The page said the bounty launched in March 2023.

Stats shown that day: 5 assets in scope, 75 hackers thanked, 19 reports resolved, last report resolved displayed as 6 days before the fetch, 122 reports received in 90 days, $23,400 paid in 90 days, $58,400 total bounties paid, average bounty $200, top bounty range $3,000–$20,000.

The page said the program has **not** committed to the platform standard "Multiple reports on systemic vulnerabilities," so severity or outcome for that kind of report may differ. Other platform standards are on [HackerOne's platform-standards article](https://docs.hackerone.com/en/articles/8369826-detailed-platform-standards).

## In scope

The policy text says the program recognizes research on eero consumer electronics and the associated device and services cloud services, plus web and mobile applications.

**Devices.** All eero-branded or eero-manufactured devices sold by eero or an authorized retailer, when both of these are true:

- the device is running the latest available software, and
- the device is listed on the [eero Software Security Updates](https://support.eero.com/hc/en-us/articles/4401964665243-eero-Software-Security-Updates) article and does not have a date in the past.

**Services and apps.** Vulnerabilities on eero backend services and apps available to customers, and the supporting systems for delivery of those services (the policy names customer support and ordering). Marketing and brand sites are described as a secondary focus.

**Mobile packages named on the policy page:**

| Name | Android package | Apple iOS app ID |
| --- | --- | --- |
| eero home wifi system | `com.eero.android` | `1023499075` |

**Domains.** The policy says the program covers all eero domains owned by eero, and it says to check WHOIS before submitting an issue on a domain found with a subdomain scanner. The published scope table, as indexed on the fetch date, lists these wildcard rows as in scope, bounty-eligible, maximum severity critical:

- `*.eero.com`
- `*.e2ro.com`

Together with the two mobile packages and eero devices, that is five assets, which matches the "Assets In Scope: 5" highlight on the program page that day.

**TODO:** confirm those five rows on the live scope table before testing. A domain that fails a WHOIS check is not made in-scope by this snapshot.

## Out of scope

Quoted from the policy's scope section:

- eero uses third-party providers. The program does not give permission to test their systems. Third-party issues are assessed case by case and most likely are not eligible.
- Direct attacks against any part of AWS infrastructure are explicitly out of scope.
- Vulnerabilities in an SoC vendor's own code may not qualify unless there is a demonstrated impact on eero products.

Core Ineligible Findings are out of scope. The program page says so and points at HackerOne's platform standards. The core list is here:

https://docs.hackerone.com/en/articles/8494488-core-ineligible-findings

That article groups common non-paying findings into theoretical issues that need unlikely interaction, issues without a real-world impact, missing best-practice hardening, and hazardous testing (availability attacks, social engineering, noisy attacks, and physical attacks) that must not be attempted unless a program explicitly allows them. eero's own non-qualifying list below is in addition to that core list.

## Rewards

The page says rewards depend on severity, that HackerOne uses CVSS 3.0 to calculate severity, and that **reward decisions are up to Amazon**. It says issues may receive a lower severity because of compensating controls and context. It says the amounts in the table are the **maximum** for each severity, and that bonuses may be given at Amazon's discretion.

Per-asset maxima, as shown in the rewards summary (table last updated 11 November 2025):

| Asset | Low | Medium | High | Critical |
| --- | --- | --- | --- | --- |
| Services, Apps, Mobile | $200 | $600 | $2,000–$6,000 | $12,000–$25,000 |
| Devices | $500 | $3,000–$4,000 | $6,000–$8,000 | $20,000–$30,000 |

The same page also showed an overall band: Low $200–$500, Medium $600–$4,000, High $2,000–$8,000, Critical $12,000–$30,000. The average bounty shown that day was $200. Averages are not the maximum, and neither figure is a quote for a future report.

The policy says you must be the **first** to report an issue on an in-scope asset, and the report must not be a duplicate. A report should include the software version, the device model when one applies, a clear description, a proof of concept where one applies, and steps to reproduce. Patch suggestions are optional. You must be available for follow-up. Remediation is prioritized by risk, customer impact, and severity.

The policy says it does not reward low-severity, purely theoretical, and best-practice issues. Operational Security submissions (the examples given are leaked employee passwords and leaked business documents) are accepted for reputation points only, not a bounty.

For services and apps, the policy publishes this severity-range guide. It is a rating guide, not a test plan. The policy says the guide is not exhaustive and that eero may set severity from impact.

| Class named on the policy | Severity range on the policy |
| --- | --- |
| Remote code execution | Critical |
| SQL injection | High–Critical |
| XXE | High–Critical |
| XSS | Medium–Critical |
| Server-side request forgery | Low–Critical |
| Directory traversal / local file inclusion | Medium–High |
| Authentication or authorization bypass (broken access control) | Medium–High |
| Privilege escalation | Medium–High |
| Insecure direct object reference | Medium–Critical |
| Misconfiguration | Low–High |
| Web cache deception | Low–Medium |
| CORS misconfiguration | Low–Medium |
| CRLF injection | Low–Medium |
| Cross-site request forgery | Low–Medium |
| Open redirect | Low–Medium |
| Information disclosure | Low–Medium |
| Request smuggling | Low–Medium |
| Mixed content | Low |

Device severity, in the policy's own summary, runs from low issues without a direct customer or device impact (its example is a parental-control bypass) up to critical issues that allow remote control of a device, permanent unrecoverable failure, bypass of critical controls, or remote access to owner credentials or tokens. High and medium depend on whether access is local or remote and whether failure is temporary. The policy says compensating controls or complexity can move a finding up or down, and that an ADB demonstration is generally accepted only when it shows a behavior an app could perform.

## Non-qualifying examples named by eero

The policy says these are examples of issues it does not award:

- Descriptive error messages (stack traces, application or server errors)
- Theoretical subdomain takeovers with no supporting evidence
- HTTP 404 pages, or other non-200 pages
- Information leakage, fingerprinting, or banner disclosure on common public services
- Disclosure of known public files or directories (example given: `robots.txt`)
- Clickjacking, and issues only exploitable through clickjacking
- CSRF on forms available to anonymous users (example given: the contact form)
- Logout CSRF
- Browser autocomplete or save-password functionality
- Lack of Secure or HTTPOnly flags on non-sensitive cookies
- Weak captcha, or captcha bypass
- Forgot-password brute force and missing account lockout
- OPTIONS method enabled
- Reflected file downloads
- Missing cache control
- Host-header attack, including generic host-header examples with no evidence a remote victim can be targeted
- Directory listing
- Missing HTTP security headers (the policy links the OWASP list of useful HTTP headers)
- SSL issues named on the page: BEAST, BREACH, renegotiation, forward secrecy not enabled, weak ciphers
- Not performing rate limiting on endpoints
- Content spoofing
- PKP / HSTS preloading
- Reports that depend on outdated browsers
- SPF, DKIM, or DMARC settings, and email spoofing
- Mixed-content scripting and self-XSS

Mobile (Android and iOS) examples the policy lists as non-qualifying:

- Shared links leaked through the system clipboard
- URIs leaked because a malicious app can view opened URIs
- Absence of certificate pinning
- Sensitive data in URLs or request bodies when protected by TLS
- Lack of obfuscation
- Crashes from malformed Intents sent to an exported Activity, Service, or BroadcastReceiver (the policy says exploiting these for sensitive-data leakage is commonly in scope)
- Sensitive data stored in the app private directory
- Lack of exploit mitigations (PIE, ARC, or stack canaries)
- Path disclosure in the binary
- User data stored unencrypted on the file system
- Lack of jailbreak and root detection
- Crashes from malformed URL schemes
- Lack of binary protection (anti-debugging) and mobile SSL pinning
- Snapshot or pasteboard leakage
- Runtime hacking that is only possible on a jailbroken device
- App logging of sensitive information (logcat, console) unless a proof shows a malicious app stealing that data from logs
- Apps that allow data backups

## Rules of engagement

Behavior, as stated on the program page:

- Amazon and eero employees and contractors, and their immediate families, may not participate.
- No post-exploitation: no modification or destruction of data, no interruption or degradation of Amazon or eero services, and no pivoting with access you were not granted.
- No brute-force attacks, and no denial-of-service attacks that hinder Amazon or eero in serving customers.
- Do not compromise or test Amazon or eero accounts that are not your own.
- If you encounter user information that is not your own, stop and report it. Report what was accessed and delete the data. Do not save, copy, transfer, or otherwise use it. The policy says continuing to access another person's data may be treated as a lack of good faith.
- Do not target Amazon or eero employees or customers. That includes social engineering, phishing, and physical attacks.
- Do not test assets that involve Amazon employees in the communication. The policy says this includes support chats, including chats that appear automated.
- Do not perform physical attacks against any Amazon or eero facility.
- Comply with local law. The policy says a violation can forfeit the bounty or remove you from the program.

Testing, as stated on the program page:

- Send the User-Agent `eeroResearcher_yourh1username`, with your HackerOne username in place of `yourh1username`.
- Automated scanners are allowed only in a limited way: the User-Agent above must be set, and the tool must stay at or below **5 requests per second** to any one service. The policy says scanning without that User-Agent can get an account or IP blocked.
- Do not use third-party sites for testing. The policy's example is XSS-hunter sites. Blind testing and any other testing may use only assets you expressly own and control, and traffic must go through domains you control. The policy says using a setup you do not host yourself forfeits the reward.
- Any application-level denial-of-service testing must add a cache-buster parameter so customers are not hit directly, and it must run on infrastructure you host. The policy says otherwise the reward is forfeited. This notebook's week-1 rule is stricter: do not run denial-of-service or other availability tests. See [WEEK1.md](WEEK1.md).

Accounts, as stated on the program page:

- Create accounts with a HackerOne email: `yourh1username@wearehackerone.com`.

HackerOne's own alias article, which is separate from the eero policy, says every hacker has `username@wearehackerone.com`, and that `username+identifier@wearehackerone.com` also forwards to that hacker so they can open more than one test account without a second HackerOne profile. Use a plus-alias only for a second account you own. The eero policy text itself does not mention plus-aliases. If a signup rejects one, stop. Do not switch to an email address you do not own.

Other process notes from the policy:

- A bypass of your own earlier report can be filed as a new report. The custom field `Bypass Reference` takes the original report ID. The policy says this does not change the reward.
- Do not disclose the issue to a third party without consent. Submit it to eero through HackerOne first. The policy says issues that were disclosed publicly or to a third party first may be ineligible.
- Do not access or collect customer data. Do not exploit an issue for any purpose other than testing. If customer data is exposed by accident, notify the program of what was accessed and confirm in writing that it was deleted.

## Safe harbor

The program publishes a safe harbor. It is quoted in [LEGAL.md](LEGAL.md). It applies to good-faith research that complies with the policy, on the services and applications the policy covers. The same section says Amazon cannot authorize activity on third-party products or technology, including third-party technology inside or connected to Amazon products.

## Firmware

Device testing is in scope only on the latest available software, on a model listed on the security-updates article with a support date that is not in the past.

The release notes fetched the same day list **eeroOS v7.18.0, released 12 November 2026**, as the newest public version. The notes for that version mention improved wifi steering for stationary devices and WPA3 support for eero Built-in. The same article says updates ship on a rolling basis and reach customer networks within a few weeks of public release, so a network can still be catching up.

Check a node you own in the eero app, using the path on [How do I check my eeroOS version?](https://www.eero.com/support/articles/how-do-i-check-my-eeroos-version):

1. Open the eero app and tap the Home tab.
2. Tap that eero's nickname. The version is shown under Software updates when the node is current. An available update is labeled as such.
3. Tap Software updates. The installed version is under Current version. An offered update is shown there as well, and can be installed with Install now. Automatic install follows the preferred update time. The article says an update applies to the whole network.

The [security-updates article](https://support.eero.com/hc/en-us/articles/4401964665243-eero-Software-Security-Updates) says eero will support a device with software security updates until at least five years from a new purchase on eero.com or Amazon.com, or until the date in the table if that date is later. Devices bought somewhere else are supported until at least the date in the table. After that, further updates are a best effort, not a guarantee. When updates end, the article says the device still works and can still provide wifi. The table is described as the devices currently sold on eero.com and Amazon.com.

Support dates in that table on the fetch date. Every date below was still in the future:

| Device | Software security updates at least through |
| --- | --- |
| eero Pro | 11 March 2030 |
| eero Beacon | 11 March 2030 |
| eero (2nd Generation) | 28 April 2030 |
| eero Pro 6 | 14 July 2030 |
| eero 6 | 31 December 2031 |
| eero 6 Extender | 31 December 2031 |
| eero 6+ | 31 December 2031 |
| eero Pro 6E | 31 December 2031 |
| eero PoE 6 | 31 December 2031 |
| eero PoE Gateway | 31 December 2031 |
| eero Max 7 | 31 December 2031 |
| eero Outdoor 7 | 31 December 2031 |
| eero 7 | 31 December 2031 |
| eero Pro 7 | 31 December 2031 |
| eero PoE 7 | 31 December 2031 |
| eero Signal | 31 December 2031 |
| eero Telephone Adapter | 31 December 2031 |

A first-generation eero (the 2016 model) is **not** in that table. Under the program rule, a device has to be listed there with a date that is not in the past. A model that is absent from the current table does not meet the test this snapshot recorded. Confirm the live article before treating any hardware as eligible. This file does not claim the support article uses the words "2016" or "ineligible."
