**How to know if my bug is in scope?**

**Summary**

“In scope”, or “out of scope” are important distinctions for bugs reported on Immunefi. Becoming familiar with these terms is essential to your success as a whitehat hacker on Immunefi, especially when it comes to getting paid.

As a whitehat working independently, you must maximize your time and effort going after the right bugs. Knowing how to find in-scope bugs and not wasting time on out-of-scope ones is the key to making it worth your while.

Checking for a bug being in scope requires **two mandatory checks**:

1. Is the impact in scope? ✅
2. Is the asset in scope? ✅

For a bug to be in scope, it has to pass both of these checks (with some exceptions for programs using **Primacy of Impact** (to be discussed later).

**Assets In Scope**

For each BBP (Bug Bounty Program) listed on Immunefi’s website, you can scroll down to find the section with the heading “Assets in scope”.

This section in each BBP contains links to all of the assets (mainly smart contracts) that are considered for the bug bounty program.

**However, keep in mind that finding just any vulnerability within these contracts does NOT automatically make it in-scope. You will have to ensure that it falls within the “Impacts in Scope” section, which we’ll discuss shortly.**

Assets that are NOT listed here, such as web servers, website frontends, subdomains, telegram etc. are generally considered NOT in-scope and would likely not result in a paid bounty.

If a web server, website frontend, subdomain, telegram, etc. is explicitly listed here, it could be considered in-scope if it falls within the “Impacts in Scope”.

**Impacts in Scope**

Similarly, for each BBP listed on Immunefi’s website, you can scroll down to find the section with the heading “Impacts in scope”.

This section in each BBP shows the different types of impacts that are accepted as in-scope. These accepted impacts are also classified differently based on the severity classification system of this bug bounty program, so you’ll know what the expected reward is for each bug.

These are listed near the top of each BBP, in the “Rewards by Threat Level” section.

Now that you know about both “Assets in scope”, and “Impacts in scope”, let’s discuss how you can put this knowledge to use!

**Setting yourself up for success**

Before you start hunting on a particular project, have a read through both the “assets in scope” and “impacts in scope” tables and become familiar with them. This will help you waste less time on unpayable bug finds, and focus on the ones that will make it worth your while.

One last thing!

**Primacy of Impact.**

Projects using **Primacy of Impact** can *sometimes* accept vulnerabilities that are NOT listed as in-scope on either the “Assets in scope” table, or the “Impacts in scope” table — provided that you can prove that the vulnerability causes **direct loss of funds** to the project.

**I believe my bug falls under Primacy of Impact. What should I do?**

So, you’ve checked that your bug might not be included as one of the listed impacts in scope, or assets in scope. But you do see that it causes **direct loss of funds** to the project, and the project uses Primacy of Impact in their BBP.

This means that you CAN report the bug, but do prepare a PoC (Proof of Concept) that demonstrates your bug and its impact.

**What if my bug is out of scope?**

If the vulnerability you found is out of scope, here’s what you can do:

1. **Report the bug anyways, but don’t expect a reward** — As a whitehat, we don’t expect you to work for kudos alone. But there are times when you may make a personal decision to submit a bug anyway, for the good of the users, or to boost your rep. Sometimes, projects may even make a goodwill payment for your positive action.
2. **Hang on to the bug** — Store it in a secure location privately. There’s always a chance that the situation changes, and the bug eventually becomes in-scope. You can report it when it does. Even if the impact or asset is not in-scope, it could still cause real damage to the protocol. Avoid discussing the details of the bug with any other parties.

**What if my bug’s impact isn’t immediately applicable?**

There are cases where your bug seems like it would be in-scope, except that it depends on a deployment, value setting, or code change that has to be made in future for the bug to be impactful. **This is highly situational.**

Submitting a bug that is theoretically in-scope **will not guarantee** you a payout, even if you make a good argument, as the outcome can differ greatly depending on circumstance. For example, it is possible that a product launch is being canceled internally due to some other reason, such as budget or priority changes.

Your next steps could be the following:

1. If you believe the changes are very likely (e.g. based on a series of public tweets/product announcements/launch schedule that has been shared by the project) and will happen soon — you can submit the bug, and be prepared to make your reasoning very clear based on those public materials.
2. The project may refute this to be improbable based on some reason (e.g. internal decision-making, lack of incentive, changes in roadmap). However, if you are unsure of the veracity of these claims, **request for Immunefi mediation to verify that this is true.**