# pip security digest — Monthly review

## Advisory

Lead advisory for this month's review — the most severe pip (Python) package advisory currently listed in GitHub's advisory database. Several advisories tied at critical severity; per our review policy the first one listed was taken as the lead.

| Field | Value |
|---|---|
| GHSA id | GHSA-w5f2-9q9c-ff4h |
| CVE id | CVE-2026-105192 |
| Affected package | lmcache (pip) |
| Severity | critical |
| Vulnerable version range | >= 0.3.9, < 0.5.6 |
| First patched version | 0.5.6 |

Summary: LMCache: Remote code execution via unsafe deserialization in multiprocess mode transport. Unauthenticated remote code execution via pickle deserialization on the multiprocess ZMQ transport (CVSS 3.1: 9.8, CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H; CWE-306).

Shortlist of other advisories tied at critical severity (not pursued as the lead under our "first listed wins" rule):

- GHSA-h4mw-j7qp-8mwm — claude-agent-sdk (CVE-2026-96620)
- GHSA-9mp3-24cc-77mg — praisonai (CVE-2026-61445)
- GHSA-2xv2-w8cq-5gxw — praisonai

## Maintainer

The lead package `lmcache` is maintained under a GitHub organization:

- Organization login: **LMCache**
- Profile link: https://github.com/LMCache

## Remediation

- [ ] Upgrade lmcache to the patched version **0.5.6** (all workers and servers together — the wire format changed in this release)
- [ ] Audit our dependency pins for any lmcache version in the range >= 0.3.9, < 0.5.6
- [ ] Add a CI dependency check so vulnerable pip packages fail the build

## Sources

- Advisory record: GHSA-w5f2-9q9c-ff4h — https://github.com/advisories/GHSA-w5f2-9q9c-ff4h
- Advisory record (tied, shortlist): GHSA-h4mw-j7qp-8mwm — https://github.com/advisories/GHSA-h4mw-j7qp-8mwm
- Advisory record (tied, shortlist): GHSA-9mp3-24cc-77mg — https://github.com/advisories/GHSA-9mp3-24cc-77mg
- Advisory record (tied, shortlist): GHSA-2xv2-w8cq-5gxw — https://github.com/advisories/GHSA-2xv2-w8cq-5gxw
- Organization profile: LMCache — https://github.com/LMCache
