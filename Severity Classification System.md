**Severity Classification System**

Bugs are assigned a severity based on the type of vulnerability that they exploit and the potential impact that they could cause. Low severity reports earn smaller rewards because the potential for damage to your project is low, whereas critical severity reports earn bigger rewards because they help to prevent major damage to the project or a direct loss of funds.

Initially, the severity level of a report is designated by you when you submit the report. However, projects are able to change the severity level if they disagree with you.

If you and the project are unable to agree on the severity level, you can request help from Immunefi.

The full list of severity classification systems used by projects on Immunefi is available.

**Severity Classification Impact Definitions**

Bugs are classified on a 4-level scale:

- Critical
- High
- Medium
- Low

This scale encompasses all the aspects of a bug, from the consequence of a successful exploit, to the level of access required to exploit it, to the probability that an exploitation attempt will be successful.

Keep in mind that if the exploit requires elevated privileges or uncommon user interaction, the level of the bug may be downgraded to reflect that.

Please note that the following impacts and explanations may be subject to change.

**Blockchain/DLT**

**Critical**

- **Network not being able to confirm new transactions (Total network shutdown)**: This attack would successfully interrupt the network’s ability to create new blocks and confirm new transactions, making the entire network unusable and potentially resulting in a shutdown.
- **Unintended permanent chain split requiring hard fork (Network partition requiring hard fork)**: This is the case when a potential attack’s damage is proven to be irreversible, and the only possible fix is splitting the network on a hard fork. A hard fork is a radical change to a network’s protocol that makes previously invalid blocks and transactions valid, or vice-versa.
- **Direct loss of funds**: This attack could allow direct theft of the native and non-native balances belonging to a user or the protocol account(s). This also applies in pass-through cases where the chain is vulnerable, but projects building on the chain hold funds.
- **Permanent freezing of funds (fix requires hardfork)**: This attack could permanently lock the network’s funds, so the only possible fix would require a hard fork.

**High**

- **Unintended chain split (Network partition)**: An attack that can impact both individual nodes and the whole network by tampering with transactions before pushing them to peers. Another example of such an attack would be a vulnerability that allows for the creation of the same block at nearly the same time by different miners, validators, or equivalent on the respective network.
- **Temporary freezing of network transactions by delaying one block by 500% or more of the average block time of the preceding 24 hours beyond standard difficulty adjustments**: This attack would successfully delay the creation of a new block and confirm new transactions, during a period of at least 500% more than the average block time of the last 24 hours. This excludes any delays happening due to the network's difficulty adjustment.
- **Causing network processing nodes to process transactions from the mempool beyond set parameters**: The attack forces nodes to process transactions from the mempool exceeding the node's configured parameters (e.g. Forcing them to process more transactions than its set limit, if any).
- **RPC API crash affecting projects with greater than or equal to 25% of the market capitalization on top of the respective layer**: This attack crashes RPC API endpoints in a way that prevents the underlying service from responding to requests. Such a crash is only a valid vulnerability if it affects projects in the layer with at least 25% of market cap.

**Medium**

- **Increasing network processing node resource consumption by at least 30% without brute force actions, compared to the preceding 24 hours**: This attack drives the resource consumption of nodes by 30% over the average of the last 24 hours (e.g. Exploiting configuration errors to flood the node's memory).
- **Shutdown of greater than or equal to 30% of network processing nodes without brute force actions, but does not shut down the network**: This attack does not bring down the entire network, so there are no permanent consequences to the network history or transaction processing, but it can lead to a slower and worse experience for users, as well as trouble accessing the network by some projects.
- **A bug in the respective layer 0/1/2 network code that results in unintended smart contract behavior with no concrete funds at direct risk**: This is an error in the implementation of certain smart contract processing logic that will lead to a different, unexpected behavior. However, no funds are at risk due to the bug in question.

**Low**

- **Shutdown of greater than or equal to 10% but less than 30% of network processing nodes without brute force actions, but does not shut down the network**: This attack is less significant than shutting down 30% or more of the nodes (explained above), but it can still have UX impacts on the overall network.
- **Modification of transaction fees outside of design parameters**: This impact refers to a situation where the transaction fees within a network are altered in a way that goes beyond the intended design or the rules set by the network itself. This means that the normal fee market dynamics are disrupted, which can have various consequences on the network. Some potential impacts include but are not limited to: Unfair advantage, Network congestion or Reduced security. However, the impact does not compromise the entire network.
- **Compiler bug**: Compiler bugs are issues within a compiler that, while not posing immediate security risks, affect the performance, correctness, or usability of the software development process. An instance of this may be a bug which results in code which should compile from compiling normally. Another example would be a compiler bug which results in incorrect optimization of bytecode, which does not result in immediate risk. If a compiler bug would result in an impact of another severity and can be proven to do so, the demonstrated impact should be selected instead.

**Smart Contracts**

**Critical**

- **Manipulation of governance vote result deviating from voted outcome and resulting in a direct change from the intended effect of original results**: This impact refers to a situation where the results of a governance vote within a platform are tampered with or altered, leading to a different outcome than what was originally intended by the voters on the governance voting platform. This includes issues like double voting, allowing proposals to be executed without quorum, allowing execution of proposals without any voting step, or directly manipulating the votes of other participants. An attack on governance is critical since governance typically has privileged access to sensitive protocol functionality and/or may have custody of vaults which can be drained by an attacker.
- **Direct theft of any user funds, whether at-rest or in-motion, other than unclaimed yield**: Theft of user funds is a worst case scenario for a project. An example of in-motion funds is a swap. A user is transferring funds to the contract with the full expectation to exchange them for an equivalent value of another asset. If an attacker can manipulate the system in such a way that a user incurs losses during the transfer and the attacker profits, this is considered direct theft of user funds. If users are losing their stake, principal, vault balances, etc, that is theft of user funds.
- **Direct theft of any user NFTs, whether at-rest or in-motion, other than unclaimed royalties**: Theft of user NFTs is a worst case scenario for a project. An example of in-motion NFTs is an NFTs that get exchanged on the market whether it is from a bid or an offer. A user is giving NFT approval to the contract with the full expectation to exchange them with other assets that were set by the user. If an attacker can manipulate the system in such a way that the user gets nothing or less than the price that was set by the user, this is considered direct theft of user NFTs.
- **Permanent freezing of funds**: This includes bricking a contract which holds tokens so that a user is no longer able to withdraw their funds. It may also include burning of funds so that they can no longer be accessed by the owner. This also includes things like self-destructing implementation contracts so that the proxy becomes useless. The impact here is that funds within a system are no longer accessible.
- **Permanent freezing of NFTs**: This includes bricking a contract which holds NFT tokens so that the owner is no longer able to interact with the NFT. It may also include burning of NFT tokens without permission from the owner of the NFT, and self-destructing the implementation contract so that the proxy which holds the NFT becomes useless. The impact here is that the NFTs within the system are no longer accessible.
- **Unauthorized minting of NFTs**: Unauthorized minting can have an impact where a user can mint more NFTs than they should, or they can mint NFTs without supplying any token.
- **Predictable or manipulable RNG that results in abuse of the principal or NFT**: This attack gives the attacker an unfair advantage over the rarity of the NFT because it is often the case that the rarity of an NFT is determined using RNG. The attacker can leverage this attack vector by setting up a front-running bot.
- **Unintended alteration of what the NFT represents (e.g. token URI, payload, artistic content)**: Some NFTs store a link on the smart contract level which refers to the actual content of the NFT. Unintended alteration means that a user is able to manipulate the representation value of the NFT, which makes the NFT display content that may not belong to that NFT.
- **Unintended consequences from Maximal-extractable value (MEV) exploration (this impact only exists on Severity Classification System v2.2)**: MEV is a measure of the profit a miner (or validator, sequencer, etc.) can make through their ability to arbitrarily include, exclude, or re-order transactions within the blocks they produce. This can include front running, sandwich attacks, and liquidations. An opportunity for MEV means that somebody not participating in the protocol is making a profit. In some circumstances (such as projects with relayers, metatransactions, liquidations, keepers, etc.) this may be a core part of the protocol, in which case that specific opportunity may be excluded from the scope.
- **Protocol Insolvency**: Some protocols provide yield to some users that is paid by other users (e.g. Compound lenders are owed yield that is provided by borrowers). An error in this calculation could result in the amount owed **to** users exceeding the amount owed **by** other users. This is insolvency. Alternatively, the protocol could have debts that exceed its assets in other ways. Of course this does not include "bank run" situations where it’s temporarily not possible to withdraw money from the protocol, but the protocol is otherwise adequately collateralized

**High**

- **Theft of unclaimed yield**: A yield is any asset distributed as a reward for participation in a system. Any theft of these rewards before they are distributed or claimed is classified as theft of an unclaimed yield.
- **Theft of unclaimed royalties**: Royalties are any asset distributed as a reward for participation in a system. Any theft of these rewards before they are distributed or claimed is classified as theft of unclaimed royalties.
- **Permanent freezing of unclaimed yield**: A yield is any asset distributed as a reward for participation in a system. Whenever an attacker can prevent the yield from being able to move from the contract, for example by making the harvest() function always fail, this would mean the yield is permanently frozen.
- **Permanent freezing of unclaimed royalties**: Royalties are any asset distributed as a reward for participation in a system. Whenever an attacker can prevent the royalties from being claimed by a user permanently, the unclaimed royalties are considered to be frozen.
- **Temporary freezing of funds**: This classification refers to temporary freezing of funds belonging to the protocol or another user, which the attacker does not own. There may be an amount of time or number of blocks which is in an acceptable range of operation for a project and is therefore excluded from consideration under this impact; however, this range of operation should be kept as short as possible because attacker locked funds can significantly impact user experience and cause rippling issues for a protocol. If an attacker needs to submit many costly transactions to achieve this impact, it is instead "Griefing" and is classified as "Medium".
- **Temporary freezing NFTs**: This classification refers to temporary freezing of user NFTs, which the attacker does not own. Whenever an attacker can prevent the NFTs from being accessible by the user by moving them to another address that is still controllable by the protocol, the NFTs will freeze temporarily and the protocol can return them to their original place.

**Medium**

- **Smart contract unable to operate due to lack of token funds**: This classification refers to bugs that mark the smart contract as unable to operate or work correctly due to lack of token funds. There may be cases where the smart contract cannot pay out any rewards for staked tokens because the contract doesn't hold any funds or won't accept any reimbursements. Another example would be the LINK token required to pay for certain Chainlink services. If those services are required for proper function of the system and it's possible (or likely) for the funds to be depleted, that would be a vulnerability.
- **Block stuffing**: this classification refers to a situation where an attacker can create many transactions that will go into one block or win flashbots auction to take the whole block, to disallow anyone else from making transactions to smart contracts.
- **Griefing (e.g. no profit motive for an attacker, but damage to the users or the protocol)**: Griefing is when the attacker calls certain functions of the smart contract that would put it in a suboptimal state, thus blocking normal function execution for any user. This would cause the user to lose money for sending the transaction, but when the smart contract is back to normal, the user would be able to call the function once again to complete it. In this instance, the attacker damaged the user by requiring them to send another transaction. The attacker does not profit, but they do damage the users or the protocol.
- **Theft of gas**: Theft of gas occurs when an attacker makes a relayer that executes a call on an attacker-controlled contract consume much more gas than they should **and** that gas is used for the benefit of the attacker. Another instance of this occurring would be when relayers are misconfigured and accept high gas limits. In this case, the attacker could use those high gas limits to make the relayers execute unrelated, complex transactions that would use gas up to that limit for their own benefit.
- **Unbounded gas consumption**: Any looping done over an arbitrarily sized array may be vulnerable to unbounded gas consumption. If an attacker can add enough items to cause the gas used to call the function to exceed the block gas limit, it can result in a denial of service attack and prevent the function from being called.

**Low**

- **Contract fails to deliver promised returns, but doesn't lose value**: This is when the code doesn't work as intended (i.e. there is some logic error but that logic error doesn't affect the protocol's funds or user funds). Another example would be an external function that is meant to return a value does not return the correct thing, however, this value is not used elsewhere in application logic.

**Web/App**

**Critical**

- **Execute arbitrary system commands**:
  - This impact refers to a security vulnerability in a website or application that allows an attacker to execute arbitrary commands on the underlying system. This type of vulnerability is often called arbitrary command injection. The impact of this vulnerability can be severe, as it provides the attacker with the ability to perform unauthorized actions on the affected system like Remote Command Execution (RCE).
- **Retrieve sensitive data/files from a running server such as**:
  - /etc/shadow
  - database passwords
  - blockchain key
  - (this does not include non-sensitive environment variables, open source code, or usernames)
    - This impact allows an attacker to access and retrieve sensitive data or files from the affected server. This type of vulnerability is often called "information disclosure" or "data leakage." The impact of this vulnerability can be significant, as it exposes sensitive information that can be used for malicious purposes or further attacks.
- **Taking down the application/website**
  - An attack that results in the disruption or complete unavailability of a website or application. This impact is different from DoS as it only refers to a vulnerability found in the application logic/code. When a website or application is taken down, it affects the user experience and the ability of users to access services and resources provided by the affected application. This can lead to customer dissatisfaction and potential loss of revenue for businesses that rely on the availability of their online services. The longer the downtime, the greater the potential negative impact on both users and the organization behind the website or application.
- **Taking down the NFT URI**
  - An attack that results in the disruption or complete unavailability of a specific NFT (Non-Fungible Token) URI (Uniform Resource Identifier). The URI is typically used to store and provide access to the metadata and associated media (such as images, videos, or other digital assets) for an NFT. When the NFT URI is taken down, it affects the ability of users to access the metadata and media associated with that particular NFT. This can lead to a poor user experience and potential loss of value for the NFT holder, as the digital asset becomes inaccessible or its provenance becomes unclear. The impact of taking down the NFT URI can be particularly significant for NFT-based digital art, collectibles, or virtual goods, where the value of the NFT is primarily derived from its unique digital content.
- **Taking state-modifying authenticated actions (with or without blockchain state interaction) on behalf of other users without any interaction by that user, such as**:
  - Changing registration information
  - Commenting
  - Voting
  - Making trades
  - Withdrawals, etc.
  - Changing the NFT metadata
    - The attacker found a way to bypass the access control protection and arbitrarily update the other data without any interaction requirement. An attacker is able to perform actions that modify the state of the system or the network on behalf of other users, without the users' knowledge or consent.
- **Subdomain takeover with already-connected wallet interaction**
  - This impact refers to a security vulnerability where an attacker gains control over a subdomain of a website or application, particularly one that interacts with users' connected cryptocurrency wallets. This takeover allows the attacker to manipulate the content and functionality of the subdomain, potentially leading to unauthorized interactions with the connected wallets.
- **Direct theft of user funds**
  - It refers to a security vulnerability or an attack that results in the unauthorized transfer or misappropriation of users' digital assets, such as cryptocurrencies or tokens, directly from their wallets or accounts. One way someone can do this is by making unauthorized calls on the RPC. RPC is a communication method used to interact with blockchain nodes for sending transactions, querying data, and performing other actions. If there is a vulnerability or misconfiguration in the RPC implementation, an attacker might exploit it to directly steal user funds.
- **Malicious interactions with an already-connected wallet such as**:
  - Modifying transaction arguments or parameters
    - The attacker found a way to substitute the contract address with a malicious contract address stored at the frontend level.
  - Substituting contract addresses
    - The attacker found a way to modify the parameters of the transaction calls made to the wallet connected to the front end.
  - Submitting malicious transactions
    - The attacker found a way to inject malicious javascript code into the frontend that could initiate a malicious transaction to the wallet connected to the frontend
- **Direct theft of user NFTs**
  - Same as with the Direct theft of user funds, but it involves stealing NFTs.
- **Injection of malicious HTML or XSS through NFT metadata**
  - This refers to a security vulnerability in which an attacker is able to inject malicious code or content into the metadata of a Non-Fungible Token. NFT metadata typically includes descriptive information about the NFT, such as title, description, and links to associated media like images, videos, or audio files. The front-end doesn’t handle/validate the content of the NFT metadata, leading to vulnerabilities like HTML or javascript injection.

**High**

- **Injecting/modifying the static content on the target application without Javascript (Persistent) such as**:
  - HTML injection without Javascript
  - Replacing existing text with arbitrary text
  - Arbitrary file uploads, etc.
    - The attacker discovered a method to persistently inject HTML code or plain text into the frontend, which could potentially deceive users visiting the frontend into providing sensitive keys, navigating to an external site controlled by the attacker, or falling for phishing schemes, among other risks.
- **Changing sensitive details of other users (including modifying browser local storage) without already-connected wallet interaction and with up to one click of user interaction, such as**:
  - Email or password of the victim, etc.
    - The attacker found a way to change the sensitive details of the victim by exploiting a Cross-Site Request Forgery (CSRF) vulnerability in the website or application. By having the victim click on a malicious link (1-click), the attacker is able to perform actions on the victim's behalf, such as modifying their stored data on the decentralized application (DApp)
- **Improperly disclosing confidential user information such as**:
  - Email address
  - Phone number
  - Physical address, etc
    - The attacker found a way where he is able to retrieve the PII or sensitive details of other users without user interaction.
- **Subdomain takeover without already-connected wallet interaction**
  - The attacker found a way to claim or hijack the subdomain and inject a malicious code that could be used as a phishing vector for victims visiting the subdomain.

**Medium**

- **Changing non-sensitive details of other users (including modifying browser local storage) without already-connected wallet interaction and with up to one click of user interaction, such as**:
  - Changing the first/last name of the user
  - Enabling/disabling notifications
    - The attacker found a way to change the sensitive details of the victim, whereby the victim clicks(1-click) the link submitted by the attacker and the attacker could be able to modify the stored data of the victim on the DAPP. This is mostly using vulnerabilities like cross-site request forgery (CSRF).
- **Injecting/modifying the static content on the target application without Javascript (Reflected) such as**:
  - Reflected HTML injection
  - Loading external site data
    - The attacker found a way to inject reflected HTML code or plain text into the frontend that could potentially be used to trick the victims visiting the frontends into submitting sensitive keys, visiting the externally attacker-controlled site or phishing, etc. This attack requires a one-click user interaction where the victim clicks the link provided by the attacker and the frontend renders the reflected HTML code provided by the attacker.
- **Redirecting users to malicious websites (Open Redirect)**
  - The attacker found a way where he could redirect the victims to an external site using the in-scope asset endpoints. The victim visits the links provided by the attacker and can be used for phishing.

**Low**

- **Changing details of other users (including modifying browser local storage) without already-connected wallet interaction and with significant user interaction such as**:
  - Iframe leading to modifying the backend/browser state (must demonstrate impact with PoC)
    - The attacker found a way to change the sensitive or non-sensitive details of the victim stored on the DAPP where victims click the link submitted by the attacker and the attacker could be able to leverage the victim's clicks(significant user interaction) to modify the stored data of the victim on the DAPP, this is mostly using vulnerabilities like clickjacking.
- **Any impact involving a publicly released CVE without a working PoC**
  - *The attacker found a vulnerable component with significant proof of the existence of the vulnerability for which the POC has not been publicly disclosed.*
- **Taking over broken or expired outgoing links such as**:
  - Social media handles, etc.
    - This refers to a situation where an attacker gains control over external links on a website or application that are no longer functional or have expired. These links might point to resources like social media profiles, external websites, or other online services. When a link becomes broken or expired, it can create an opportunity for an attacker to register or claim the associated resource, essentially taking over the destination of the link.
- **Temporarily disabling user to access target site, such as**:
  - Locking up the victim from login
  - Cookie bombing, etc.
    - An attack that results in the temporary prevention of a user from accessing a website or application. This can occur through various methods, such as preventing the user from logging in or using techniques like cookie bombing to disrupt the user's access. The impact of this vulnerability or attack is that it negatively affects the user experience and may cause frustration or inconvenience, as users are temporarily unable to access the desired services or resources on the target site.