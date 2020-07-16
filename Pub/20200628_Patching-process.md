# Patching process

## General
- First there's no universal solution, the following sections are my views on this subject.
- Patching without understanding your risks are useless, doing that first.

## Patching
- Attackers will try to gain access 90% of time through two vectors:
  * Exposed services / devices on the internet
  * Email

- These two entry points are the critical ones, the patching should be prioritized or mitigation measures / detection measures enhanced on these.

### Exposed services
- Know which devices you are exposing on the internet
- Know the more details you can on how the vulns can be exploited:
  - Need an account or unauthentified ?
  - Standard deployment or personalized settings ?
  - Exploitation is simple or need some luck or numerous attempts to succeed ?
  - Exploit is publicly available ?
  - Is it another try to patch a known vulnerability (Sometimes, a software company don't patch the vuln but mitigate it by adding in software requests parser detection of known exploit strings / parameters, they don't patch the root of the vuln)
  - 
  
- Know the value of the asset, prioritize high valuable assets
- Deny access to non necessary ports
- Know which accounts are used on them, watched their utilization carefully
- Know which software are used and follow their updates
- Know also the dependencies on which these software are built with (Sometimes, a vuln is identified in OSS packages, big software players used this package but patched the vulnerability long times after)

TBC
