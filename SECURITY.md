# Security Policy

TrustMint includes Soroban contracts that demonstrate asset tokenization and compliance workflows. The code has not received an independent security audit. Do not treat this repository as production-ready or use it to custody real assets without an independent review.

## Report a vulnerability

Please do not disclose suspected vulnerabilities in public issues or pull requests. Use [GitHub’s private vulnerability reporting](https://github.com/zeemscript/TrustMint/security/advisories/new). If private reporting is unavailable, contact the repository maintainers through their GitHub profiles and ask for a private reporting channel.

Include the affected contract or component, the commit or version, reproduction steps, and the possible impact. Please avoid testing against public deployments or accounts you do not control.

The maintainers will acknowledge reports and coordinate investigation and disclosure with the reporter. No response-time guarantee is currently published.

## Scope

This policy covers the TrustMint contracts, SDK, deployment tooling, and frontend maintained in this repository. Third-party dependency vulnerabilities should be reported to their respective maintainers. Reports about a live deployment should identify the network and contract IDs; do not include private keys, recovery phrases, or personal identity documents.

## Supported code

Security fixes are made against the latest code on `main`. Older tags, forks, and deployed contracts do not update automatically. Contract operators are responsible for assessing and applying upgrades or redeployments.
