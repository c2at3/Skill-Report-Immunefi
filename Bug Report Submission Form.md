0. Scope & Asset
**Asset**: ...

**Choose Impact(s) - Smart Contract**
View Impact Definition
Choose one or more impacts that apply to your vulnerability.
Direct theft of any user funds, whether at-rest or in-motion, other than unclaimed yield
Temporary freezing of funds
Theft of user fees
Denial of service attacks
Loss of bridge or staking funds
Temporary freezing of funds for less than 1 week
Theft of unclaimed yield
Permanent freezing of unclaimed yield
Smart contract unable to operate due to lack of token funds
Block stuffing for profit
Griefing (e.g. no profit motive for an attacker, but damage to the users or the protocol)
Theft of gas
Unbounded gas consumption
Any governance voting result manipulation
Direct theft of any user funds, whether at-rest or in-motion, other than unclaimed yield
Permanent freezing of funds
Miner-extractable value (MEV)
Protocol insolvency

**Choose Impact(s) - Blockchain/DLT**
View Impact Definition
Choose one or more impacts that apply to your vulnerability.
Permanent freezing of funds (fix requires hardfork)
Direct loss of funds
Transient consensus failures
Network not being able to confirm new transactions (total network shutdown)
Denial of service attacks

**Choose Impact(s) - Websites & Apps**
View Impact Definition
Choose one or more impacts that apply to your vulnerability.
Ability to execute system commands
Extract Sensitive data/files from the server such as /etc/passwd
Taking down the application/website
Stealing User Cookies
Bypassing Authentication
Signing transactions for other users
Redirection of user deposits and withdrawals
Subdomain takeover resulting in financial loss (applicable for subdomains with addresses published)
Wallet interaction modification resulting in financial loss
Direct theft of user funds
Tampering with transactions submitted to the user’s wallet
Submitting malicious transactions to an already-connected wallet

1. Title
Try to use a vulnerability classification and the impact. For example, "Reentrancy in the withdraw function leads to total loss of funds", or "Lack of access control in the update function leads to griefing." After reading the title, the program should understand the basics of what the bug report is about.

2. Description
The more details you provide, the faster and more accurately the program can assess your bug report. You should put yourself in the shoes of the program team and ask yourself the question, "Am I describing the vulnerability and its impact clearly, accurately, and without any unnecessary assumptions?"

## Brief/Intro
Provide a very short and concise (one paragraph) statement on what the problem is, and what the consequences would be if the bug were exploited in production/mainnet.

## Vulnerability Details
Offer a detailed explanation of the vulnerability itself. Do not leave out any relevant information. Code snippets should be supplied whenever helpful, as long as they don’t overcrowd the report with unnecessary details. This section should make it obvious that you understand exactly what you’re talking about, and more importantly, it should be clear by this point that the vulnerability does exist.

## Impact Details
Provide a detailed breakdown of possible losses from an exploit, especially if there are funds at risk. This illustrates the severity of the vulnerability, but it also provides the best possible case for you to be paid the correct amount. Make sure the selected impact is within the program’s list of in-scope impacts and matches the impact you selected.

## References
Add any relevant links to documentation or code

2. Proof of Concept
## Proof of Concept
Secret Gist: `https://link`
Add a secret Gist environment to support your PoC (optional)
To help programs evaluate your report easier, we recommend linking to a Gist. Gists are not a replacement for your PoC and they must be made secret. Learn about gists or create one from the command line.

Providing a runnable PoC for your Bug Bounty reports is crucial because it shows that the vulnerability is real. For Solidity smart contracts, you are welcome to use our PoC templates (https://github.com/immunefi-team/forge-poc-templates). For standard Bug Bounty Programs, all PoCs must follow the PoC Guidelines and Rules (read in Proof of Concept (PoC) Guidelines and Rules.md). Breaking these rules may result in your report being rejected as well as action potentially taken against your account.


> Spam Warning: Many reports from new accounts are flagged as AI-generated or low-quality. Submissions without a clear, original explanation and a working proof-of-concept are likely to be rejected.