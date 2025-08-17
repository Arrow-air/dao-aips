# AIP-001 

---
AIP: 1
title: AIP Purpose and Guidelines
description: Information on Arrow Improvement Proposals (AIPs) and the AIP process
author: Sleety (https://github.com/sl33ty)
discussions-to: https://dao.arrowair.com/t/AIP-001-discussion-aip-purpose-guidelines/24
status: Living
type: operational
created: 2024-08-05
vote-to: https://snapshot.org/#/arrowair.eth/proposal/0x156f8939f6937932a4b3cab44592cdd38a79bd422974cef88f84baad2195e389
vote-date: 2024-09-12
vote-result: Passed
---

## Summary: What is an AIP?
AIP stands for Arrow Improvement Proposal. An AIP is a design document providing information to the Arrow community or describing a new feature for Arrow. We intend for AIPs to be the primary mechanism for proposing new features and documenting the operational and organizational improvements of Arrow DAO.

The precise format for AIPs is detailed below, and a template is located [here](https://github.com/Arrow-air/dao-aips/blob/main/AIP-template.md)

Only AIPs in the “Final” state are eligible for adoption and must be reviewed by editors before marked as “Final”. If you want to contribute to an existing “Draft” AIP, coordinate with the original author(s) to submit a PR. If you want to work on a new AIP, contact any of the AIP editors listed [here](https://github.com/Arrow-air/dao-aips/blob/main/AIPs/AIP-003.md)

**The AIP author is responsible for building consensus within the community and documenting dissenting opinions.**

## AIP Work Flow

### Shepherding an AIP
Parties involved in the process are you (i.e. the champion or AIP author), the AIP Editors, and the Arrow community.

Before you begin writing a formal AIP, you should vet your idea. Ask the Arrow community on the [Discord server](https://discord.gg/arrow) or [DAO Forum](https://dao.arrowair.com/c/arrow-improvement-proposals) first if an idea is original to avoid wasting time on something that will be rejected based on prior research. 

It is highly recommended that a single AIP should contain a single key proposal or new idea. The more focused the AIP, the more successful the ensuing process tends to be. Template for new AIPs is available [here](https://github.com/Arrow-air/dao-aips/blob/main/AIP-template.md).

Once the idea has been vetted, your next responsibility will be to present a Draft AIP to the Arrow community to begin the first tracked stage of the AIP process. This draft can exist as a work in progress by the Author and can remain in an incubation state if the idea or implementation needs to be developed further. Once the document is mature and ready for wider community feedback it goes to the Review stage i.e. ready for review/constructive feedback.

During the review stage more collaborative editing can occur based on feedback from the wider community. At the end of the review stage it is advised to conduct an informal poll to gauge if there is positive sentiment around the AIP document as it currently exists.

If the sentiment poll result is positive and all feedback has been considered, AIP Editors will announce a Last Call for the AIP. The Last Call stage is the community's last chance to suggest amendments to the proposal document.

If new substantial changes are suggested and require further discussion, the document should move back to Review. If no substantial changes are required, the document will be ready for token voting at the end of the Last Call period.

The snapshot vote will be created by AIP Editors along with vote text according to [these template headings](#snapshot-vote-text).

If the vote is passed, AIP Editors change the AIP's status to 'final' or 'living'. If the vote does not pass, AIP Editors will give the document a status of 'stagnant' (if no longer being actively worked on) or 'draft' (if it is still being worked on).

### AIP Process

The following is the standardization process for all AIPs:

**Draft** - The first tracked stage of an AIP in development. A Draft AIP is merged by an AIP Editor into the AIP repository once properly formatted.

**Review** - Reached once an AIP Author marks an AIP as ready for Review. This period is concluded with a community sentiment poll, prior to inclusion in the AIP repo and final token vote to affirm implementation.

**Last Call** - a short period where AIP document is prominently displayed as the final proposal that will be voted on if no substantial changes are requested.

**Final** - A Final AIP exists in a state of finality and should only be updated for spelling or grammar corrections and additional context, not for consequential changes. 

**Stagnant** - Any AIP in Draft or Review which is inactive for too long is moved to Stagnant. An AIP may be resurrected by simply requesting this status change from an [AIP Editor] (link)

**Withdrawn** - The AIP Author(s) have withdrawn the proposed AIP. This state has finality and can no longer be resurrected using this AIP number. If the idea is pursued at a later date it is considered a new proposal.

**Living** - A special status for AIPs that are designed to be continually updated and not reach a state of finality. This includes most notably AIP-001 (AIP Purpose & Guidelines).

**Obsolete** - An Obsolete AIP has been replaced, superseded or removed.
Only Final and Living AIPs are eligible for official adoption.

![AIP Process Diagram](https://raw.githubusercontent.com/Arrow-air/dao-aips/main/assets/aip-001/AIP-process-diagram.png)

## AIP Templates and Formats

### AIPs
AIPs should be written in markdown format. AIP Template available [here](https://github.com/Arrow-air/dao-aips/blob/main/AIP-template.md)

### AIP Header Preamble

Each AIP must begin with a header preamble, preceded and followed by three hyphens (---). This header is also termed “front matter” by Jekyll. The headers must appear in the following order.

`AIP`: AIP number (this is determined by the AIP editor)

`title`: The AIP title is a few words, not a complete sentence

`description`: The AIP description, in one or two short sentences.

`author`: The list of the author’s or authors’ name(s) and/or username(s), or name(s) and email(s). Details are below.

`discussions-to`: The url pointing to the official discussion thread on dao.arrowair.com

`status`: Draft, Review, Final, Stagnant, Withdrawn, Living, Obsolete

`type`: One of Operational or Informational.

`created`: Date of AIP  number assignment in yyyy-mm-dd format, e.g. 2001-08-14

`withdrawal-reason`: An optional sentence explaining why the AIP was withdrawn.

`vote-to`: If this AIP had a concluded vote, the url pointing to the vote (e.g. snapshot url) For a Living AIP that has had a successful vote, this should be the address of the last "Passed" vote.

`vote-date`: If this AIP had a concluded vote, when that happened in yyyy-mm-dd format. For a Living AIP that has had a successful vote, this should be the date when the last "Passed" vote concluded.

`vote-result`: If this AIP had a concluded vote, the result of the ("Failed" or "Passed"). For a Living AIP that has had a successful vote, this should remain "Passed".

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

### `author` header

The `author` header lists the names, email addresses or usernames of the authors/owners of the AIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the `author` header value is:

    Random J. User (GH: githubname | Discord: discordname) <address@dom.ain>

Authors are not required to provide a GitHub username, Discord tag, or email; however, at least one author must provide a GitHub username in order to get notified on change requests and to approve or reject them.

## Snapshot Vote Text

The following headings are recommended when creating the Snapshot vote text.

- Brief description of AIP
- Rationale
- Outcome if Vote Passes
- Outcome if Vote doesn’t pass
- Relevant Resource Links
- Discussion Links
- Link to the most recent version of this AIP in the AIP github repo.

## Linking to External Resources

Links to external resources **SHOULD NOT** be included. External resources may disappear, move, or change unexpectedly.

## Linking to other AIPs

References to other AIPs should follow the format `AIP-N` where `N` is the AIP number you are referring to. Each AIP that is referenced in an AIP **MUST** be accompanied by a relative markdown link the first time it is referenced, and **MAY** be accompanied by a link on subsequent references. For example, you would link to this AIP with `[AIP-001](AIP-001.md)`.

## Auxiliary Files

Images, diagrams and auxiliary files should be included in a subdirectory of the `assets` folder for that AIP as follows: `assets/aip-N` (where N is to be replaced with the AIP number - e.g. 001, 099, 240 etc.). When linking to an image in the AIP, use relative links such as `[Image Title](../assets/aip-001/image.png)`.

## AIP Editors

Current and historic AIP editors are recorded in [AIP-003](https://github.com/Arrow-air/dao-aips/blob/main/AIPs/AIP-003.md).

## AIP Editor Responsibilities

For each AIP, an editor does the following:

    Read the AIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don’t seem likely to get to final status.
    The title should accurately describe the content.
    Check the AIP for language (spelling, grammar, sentence structure, etc.), markup (GitHub flavored Markdown), code style

If the AIP isn’t ready, the editor will send it back to the author for revision, with specific instructions.

Once the AIP is ready for the repository, the AIP editor will:

    Assign an AIP number
    Merge the corresponding pull request
    Send a message back to the AIP author with the next step.

The editors don’t pass judgment on AIPs. They are necessary to do the administrative & editorial part.

## Style Guide

### AIP numbers

When referring to an AIP by number, it should be written in the hyphenated form AIP-X where X is the AIP’s assigned number (in a three-digit numerical format e.g. 001, 099, 240 etc.)

### RFC 2119

AIPs are encouraged to follow [RFC 2119](https://datatracker.ietf.org/doc/html/rfc2119) for terminology and to insert the following at the beginning of the Specification section:

    The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in RFC 2119.

## History

This document was derived heavily from Ethereum's EIP-1 written by [Martin Becze](mailto:mb@ethereum.org), [Hudson Jameson](mailto:hudson@ethereum.org), et al. which is in turn derived from Bitcoin’s BIP-0001 written by Amir Taaki which in turn was derived from Python’s PEP-0001. In many places text was simply copied and modified. Although the PEP-0001 text was written by Barry Warsaw, Jeremy Hylton, and David Goodger, they are not responsible for its use in the Arrow Improvement Process, and should not be bothered with technical questions specific to Arrow or the AIP. Please direct all comments to the AIP editors.

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

# AIP-002

---
AIP: 2
title: Creation of Grants and Bounties Committee
description: Establishing an entity to oversee coordination and payment of bounties and grants
author: Sleety (@sl33ty)
discussions-to: https://dao.arrowair.com/t/AIP-002-discussion-creation-of-grants-and-bounties-committee/31
status: Final
type: operational
created: 2024-08-01
vote-to: https://snapshot.org/#/arrowair.eth/proposal/0x2b4cfba6a52d08a8e8baf6d1228392ea03855f0bafad61e437a1d7408caa2241)
vote-date: 2024-09-12
vote-result: Passed
---

## Abstract
This proposal seeks to establish an entity to provide coordination and payment of bounty and grant incentives within Arrow DAO. The entity will be known as the Grants and Bounty Committee (hereafter GBC). This proposal outlines the operational and governance considerations required to establish such an entity.


## Motivation
There is broad agreement in the community that Arrow should move towards more grants and bounties, following [Sleety's Document](https://docs.google.com/document/d/1v2tBo8o7kI7G1R95QEQOw2BDRZg0pYDc0xC4iNkehqc/edit?usp=sharing) and subsequent discussions. Many advantages of such a system were discussed, including more accountability and transparency regarding the work of current Arrow contributors. In addition, grants and bounties can open up opportunities for new and talented people to contribute to various DAO projects. 

Arrow as a DAO was formed with the idea that anybody in the world with the expertise and enthusiasm could contribute to the mission of making air travel accessible and affordable for all. We embrace technological advances in global coordination that enable collaboration on ambitious projects that were previously impossible. We have chosen eVTOL aircraft as necessary hardware to achieve our mission. Underpinning this is a belief that building our aircraft in public, harnessing global talent and making our hardware designs open source, will help us get there quicker. The GBC entity is required to ensure that contributions flow frequently, and in the right direction. Such an ambitious scaling attempt requires a focused and organized entity to champion its implementation and improvement.


The GBC will be DAO-elected. It will be entrusted with the coordination, assessment and payment of grants and bounties in order to harness community talent and further the goals of the DAO.

Arrow requires a GBC that can:
- inform and supply resources to help Arrow community members apply for grants and bounties
- assess and appraise applications fairly
- liaise with applicants to help achieve desired result
- embrace and foster an environment where high quality contributions are welcomed, explained and celebrated 
- reject applications that are low quality or economically unfeasible
- request improvement, resubmission of incomplete/low effort applications
- meet regularly with a clear agenda to fulfill the above duties


## Specification

### Definitions
The GBC’s chief mission SHALL be to distribute Grants and Bounties, retrospectively and prospectively, in order to harness the community’s talent to further the goals of Arrow DAO.

The GBC SHALL abide by the following definitions for grants, bounties, commitment track compensation, and retrospective awards:

**Bounty Proposals**: A proposal submitted by Arrow or an Arrow Community Member that proposes a payment for an achieved result of a specific task/project. The bounty proposal SHOULD establish the desired outcome, state an award compensation amount with a payment schedule. The bounty proposal SHOULD establish the desired outcome, state an award compensation amount with a payment schedule, and describe how interested parties can compete in the selection process for the bounty. The entity that submitted the proposal MAY or MAY NOT be the person(s) awarded the bounty contract.

**Project-Based Grant**: A proposal submitted by Arrow or an Arrow Community Member that proposes some action with an estimate of cost, milestones for deliverables and payment schedule. Grants SHALL be a set amount broken up and paid over a set period. This might be X USDC + X ARROW paid over 6 months. This contract is awarded to the entity that submitted the proposal if the grant is approved.

**Time Commitment Grant**: A proposal submitted by an individual that proposes compensation for tasks and activities deemed necessary for ongoing daily work and discussions related to critical areas of the DAO. 

**Retrospective Award**: A proposal submitted by an individual or group that proposes a payment for a previously-achieved result. The retrospective award SHOULD detail the work that was completed and the positive impacts for the DAO that would merit such an award. The entity that submitted the retrospective award proposal MAY or MAY NOT be the person(s) awarded a retrospective award for the work documented in the proposal. The retrospective award SHOULD be awarded in a blend of USDC or similar stablecoin and/or ARROW token as per Time Commitment Grant compensation guidelines (see [AIP-004](https://github.com/Arrow-air/dao-aips/blob/main/AIPs/AIP-004.md)). Calculations of ARROW token amounts SHALL NOT include expenses, which are processed as reimbursement receipts.

### Difference Between Bounties & Grants

Grants are intended to be applied for by those who are wishing to carry out the work themselves. 

Bounties are open-ended goals that could be met by anyone, including those other than the proposing party. In other words, if I believed that Arrow needed a sub-scale aircraft drone for publicity purposes and I wanted to be the one to build it, I would apply for a grant. If I instead thought Arrow needed a sub-scale aircraft drone for publicity purposes but I wanted it to be open to whoever comes up with the best plan to build it and win the contract, then I’d propose a bounty.

## Awards Process
- The GBC SHALL publish an open call for Time Commitment grant applications by the second Sunday of the first month after the successful creation of the scoring rubric (see below), with deadlines for application falling on the third Sunday of that month. Subsequent calls for Time Commitment grant applications SHALL occur every second month thereafter (bimonthly), following the same second Sunday/third Sunday of the month deadline schema.

- The GBC SHALL review Time Commitment grant applications.

- The GBC SHALL review project-based grant applications.

- The GBC SHALL review bounty proposal applications.

- The GBC MAY give retrospective USDC and ARROW token awards for previously-completed work. Such applications MAY be submitted on behalf of others rather than being self-nominated. Calculations of ARROW token amounts MUST NOT include expenses, which are processed as reimbursements.

- The GBC SHALL score applications and announce proposed recipients by the final Sunday of the month after the successful creation of the scoring rubric. Subsequent announcements of proposed recipients SHALL occur every other month (bimonthly) thereafter, following the same final Sunday of the month deadline schema.

- Prior to the first call for applications, the GBC SHALL develop one or more rubrics by which to select winning grants and bounties. The rubric(s) SHALL be publicly posted and anyone interested in participating SHALL be solicited in their development. The GBC MAY choose to develop separate rubrics for project-based grants, time commitment grants, bounties, and retrospective awards.

## Guiding Principles
- The GBC's chief mission SHALL be to approve bounty and grant applications that are of high quality and further the goals of the DAO.

- The GBC SHALL manage funds and allocate funds effectively.

- The GBC SHOULD consider its long term strategy when approving or rejecting applications.

## Assessment of Awards
- Recipients of a Time Commitment grant SHALL update the GBC in a publicly-available document about their progress on at least a monthly basis (or more if their bounty/grant specifies).

- Recipients of a Project-based grant SHALL update the GBC in a publicly-available document about their progress as agreed in grant application, or at least on a weekly basis.

- If a majority of the GBC agrees that a grant recipient is failing to provide the specified services to the DAO in a timely manner (as documented in the original application and in subsequent monthly updates), the GBC SHALL publicly announce such a decision and cease any future payments. This decision MAY be disputed by anyone through the creation of an AIP within two weeks of the GBC’s announcement. The AIP SHALL be subject to a snapshot vote.

- Any group or individual MAY submit a publicly-available document to the GBC claiming successful completion of the bounty. The GBC SHALL discuss all such applications. If a majority of the GBC agrees then the GBC SHALL announce the award of the bounty. Anyone MAY dispute the awarding of the bounty through the creation of an AIP within two weeks of the GBC’s announcement. The AIP SHALL be subject to a snapshot vote.

- Grant compensation SHALL be awarded in full upon completion of stated milestones/deliverables. It is at the discretion of the GBC whether the compensation amount can be streamed to recipients via streaming payment application.

## Conflicts of Interest
The GBC SHALL act according to these processes to minimize conflicts of interest:

- Any GBC member SHALL NOT score, vote on, or participate in GBC discussions about any retrospective award for which they are nominated. They MAY participate in the ratifying snapshot vote.

- Any GBC member who submits a grant application SHALL abstain from scoring and voting on any grants during the application period for which they are an applicant.

- They may participate in discussions involving their application for the purpose of improvement, refinement and clarification only.

- They may participate in the ratifying snapshot vote. They may also score, vote, and participate in discussions in future rounds during which their grant is ongoing, provided they have not submitted an application during that round for any new grants.


## Selection and Governance of GBC
The GBC will act according to the following:

- The GBC SHALL contain a minimum of five individuals.

- The GBC SHOULD be multidisciplinary and composed of reputable and knowledgeable community members.

- The GBC SHOULD be eligible for monetary compensation via a stipend or bounty for their time.

- For the initial selection process, 5 members SHALL be selected. A list of active and historic members of the GBC SHALL be provided in a publicly-available document [see AIP-003](https://github.com/Arrow-air/dao-aips/blob/main/AIPs/AIP-003.md).

- Arrow contributors interested in becoming inaugural members of the GBC SHOULD nominate themselves through an informal voting method on the forum and/or Discord.

- The initial nominated members SHALL be accepted by a separate snapshot vote, within two weeks of the vote result for this AIP.

- Changes to the GBC membership (e.g. member leaving) SHALL follow the same process, and new membership accepted by a snapshot vote.


## Copyright
Copyright and related rights waived via CC0. https://creativecommons.org/publicdomain/zero/1.0/

# AIP-003

---
AIP: 3
title: Create Membership List
description: Proposal to create a maintainable list of current and historical committee memberships
author: Sleety (@sl33ty)
discussions-to: https://dao.arrowair.com/t/aip-003-discussion-committee-membership-record/29
status: Living
type: informational
created: 2024-07-01
vote-to: https://snapshot.org/#/arrowair.eth/proposal/0x7bd5105b1ace1cf1100cd2b6b6b1555215cbc2ad96950a5b14d25ee2171fe9a0
vote-date: 2024-09-12
vote-result: Passed
---

## Abstract
This informational AIP lists the active committees and roles within the Arrow DAO, gives a brief overview of their purpose, and provides links to further information. It also contains current and historic membership information for each of these committees and roles.

## Motivation
Currently, there is no overview of the active committees within Arrow, or their purpose. The community should be easily able to find information like committee membership and contributor responsibilities. This AIP will result in this information being presented in a more user-friendly way. Further, historical membership is not being recorded in a structured way outside of the committees themselves.

## Arrow DAO Committees and Roles
| Date Established | Committee / Role                    | Chief Mission                                           | Defining AIPs | Multisig Addresses                                           | Links / Resources |
|------------------|-------------------------------------|---------------------------------------------------------|---------------|--------------------------------------------------------------|-------------------|
| 2024-28-08       | AIP Editors                         | To manage and administer the AIP process                | AIP-001       | N/A                                                          |                   |
| 2024-22-08       | Grants and Bounties Committee (GBC) | To distribute funding to further the goals of Arrow DAO | AIP-002       | 0x7cFd3D29fD7b13CA33E49bA6b11b79bEF89e5906                   |                   |

## AIP Editors
### Current Membership
| Member Since     | Members                             | Comment                                                 |
|------------------|-------------------------------------|---------------------------------------------------------|
| 2024-01-08       | WhiteDadJokes                       | Part of first batch of editors                          |
| 2024-01-08       | Sleety                              | Part of first batch of editors                          |
<!--
| 2024-01-08       | Member 3                            | Part of first batch of editors                          |
| 2024-01-08       | Member 4                            | Part of first batch of editors                          |
| 2024-01-08       | Member 5                            | Part of first batch of editors                          |
-->

<!--
### Historic Membership
| Member Since     | Members                             | Comment                                                 |
|------------------|-------------------------------------|---------------------------------------------------------|
| 2024-01-08       | Member 6                            | Part of first batch of editors                          |
| 2024-01-08       | Member 7                            | Part of first batch of editors                          |
-->


## Grants and Bounties Committee
### Current Membership
| Member Since     | Members                             | Comment                                                 |
|------------------|-------------------------------------|---------------------------------------------------------|
| 2024-01-08       | Alperenag                           | Part of first batch of GBC members                          |
| 2024-01-08       | Errrks                              | Part of first batch of GBC members                          |
| 2024-01-08       | Sleety                              | Part of first batch of GBC members                          |
| 2024-01-08       | Thomasg                             | Part of first batch of GBC members                          |
| 2024-01-08       | WhiteDadJokes                       | Part of first batch of GBC members                          |

<!--
### Historic Membership
| Member Since     | Members                             | Comment                                                 |
|------------------|-------------------------------------|---------------------------------------------------------|
| 2024-01-08       | Member 6                            | Part of first batch of GBC members                          |
| 2024-01-08       | Member 7                            | Part of first batch of GBC members                          |
-->

## Maintaining Records
The intention is for this AIP to contain records about all active committees. For this reason, if any future committees are approved by the DAO, they should be added to this record by the AIP Editors.

# AIP-004

---
AIP: 4
title: Introduce Time Commitment Grant
description: A proposal to replace commitment track compensation with a Time Commitment Grant
author: Sleety ([@sl33ty](https://github.com/sl33ty))
discussions-to: https://dao.arrowair.com/t/aip-004-discussion-introduce-time-commitment-grant/37
status: Final
type: operational
created: 2024-09-02
vote-to: https://snapshot.org/#/arrowair.eth/proposal/0x27aab416de44ff27a1c5fc3bff826db6b1e3d7c53a573ee38374cbdfad2f74bf
vote-date: 2024-09-26
vote-result: Passed
---

## Abstract
This AIP proposes a revised purpose, process and definition of the commitment track within Arrow DAO. It also proposes a reduction in base compensation for commitment track recipients.

## Background
Contributions to Arrow DAO began in November 2021. People interested in the project began contributing significant amounts of their time and efforts on an entirely voluntary basis. In May 2022, Arrow recognized that core team working on engineering prototypes, services and growth was difficult to achieve - mostly due to people limited in the (unpaid) time they could contribute. A plan to compensate core team members for their contributions arose. 

These [compensation guidelines](https://docs.google.com/spreadsheets/d/1Mngt2VHdpZgCwRceVHUqXD9ufMx2gninVBPxm0RkXRQ/edit?usp=sharing) have been used since then and contributors who were actively contributing to Arrow in various ways such as building prototypes, attending meetings, participating in discussions, solving organizational problems etc. were allocated funds from the treasury in exchange for their ongoing commitment and availability for synchronous discussions. This compensation scheme is called 'the commitment track' and applications are processed and paid on bimonthly cycle. Contributors receive funds via an onchain streaming platform (initially [Sablier](https://sablier.com), later [LlamaPay](https://llamapay.io)) which is funded bimonthly by their respective working Pods. Each pod applies for funding form the main Arrow treasury (via Snapshot vote) to cover these expenses on a bimonthly basis.

The idea of reducing commitment track compensation was the result of discussion during the Texas meetup [May 2024] on how we could incentivize current and future Arrow contributors to be more accountable in their work. A commitment to increasing the number of bounties was proposed as a good solution, but it surfaced another issue - current commitment track contributors didn't have much of an incentive to create bounties for their own work.

## Motivation
<!---
The motivation section should describe the "why" of this AIP. What problem does it solve? Why should someone want to implement this standard? What benefit does it provide to the Arrow ecosystem? What use cases does this AIP address?
-->

For Arrow to become a decentralized organization of hundreds of active contributors, it must think carefully about the coordination of projects and tasks within the DAO. A cultural shift in the way Arrow works - towards fair reward bounties for thoughtful and important contributions, clearly defined and trackable - is generally agreed to be a good thing. For potential talented contributors seeking to add their expertise to the project in some way, a walled garden of main contributors with little accountability and little incentive to change is not an encouraging place to develop a buzzing community of builders.

The current implementation of this 'recurring payment for x amount of contributor's time' has led to valuable work being completed, however clear definition and traceability of work completed was lacking. Commitment track performance has been rarely reviewed or appraised and applications roll over without critique. The non-hierarchical DAO structure, while advantageous in other areas, presents a challenge for measuring value created, a challenge that should be mitigated by the creation of the [GBC](https://github.com/Arrow-air/dao-aips/blob/main/AIPs/AIP-002.md). 

The intention of a base compensation reduction is that Arrow benefits from retained core services that are important for sustainability, but gains a bounty system that can be built to overcome the inefficiencies we've experienced from a largely 'payroll'-type system.

## Specification

### Definition
Commitment track compensation SHALL hereafter be known as a 'Time Commitment Grant'.

### Purpose
The purpose of the **Time Commitment Grant** SHALL be to monetarily recognize and reward high performing, valued and committed contributors to Arrow DAO. This grant SHALL incentivize continued high performance, foster a culture of appreciation, ensure we attract key talent essential for the organization's sustainability and growth. 

### Base Compensation
Current base compensation guidelines can be viewed [here](https://docs.google.com/spreadsheets/d/1Mngt2VHdpZgCwRceVHUqXD9ufMx2gninVBPxm0RkXRQ/edit?usp=sharing).

Successful Time Commitment Grants SHALL be compensated using the following tables as a guide.

#### Compensation Guidelines

| Expertise Level | Hourly         |
| :-------------- | -------------: |
| `Level 5`       | $75            |
| `Level 4`       | $64            |
| `Level 3`       | $48            |
| `Level 2`       | $34            |
| `Level 1`       | $19            |

#### Weekly and Monthly Commitment Options

| Option          | Hours/wk        | Hours/Month    |
| :-------------- | :-------------- | :------------- |
| 1        | `20 hours`      | `80 hours`     |
| 2        | `16 hours`      | `64 hours`     |
| 3        | `12 hours`      | `48 hours`     |
| 4        | `8 hours`       | `32 hours`     |
| 5        | `4 hours`       | `16 hours`     |

#### Example Time Commitment Combinations

| Expertise Level | Hours/wk       | Hourly         | Monthly        |
| :-------------- | -------------: | -------------: | ------------:  |
| `Level 2`       | 12             | $34            | $1,088         |
| `Level 4`       | 16             | $64            | $1,024         |
| `Level 3`       | 20             | $48            | $3,840         |
| `Level 5`       | 8              | $75            | $2,400         |
| `Level 1`       | 4              | $19            | $304           | 

Note: Hourly rate calculations use 48 weeks (4 weeks for holidays/sickness buffer)

These base hourly rate calculations for expertise levels SHOULD be used as a guide when evaluating a bounty application's cost/benefit analysis.

### Arrow Token Percentage
Time Commitment Grant applicants MUST request a blend of USD and Arrow Tokens EXCEPT when 100% Arrow requested.

Each Time Commitment Grant MUST include a minimum of 10% allocated in Arrow Tokens. Percentages of Arrow requests MUST be in increments of 5%. For example: 10%, 15%, 20%, 25% up to 100%.

Table: Example Time Commitment Grant compensation blends:

| % USD           |  % ARROW     |
| --------------- | -------------|
| 90%             | 10%         |
| 75%             | 25%         |
| 85%             | 15%         |
| 50%             | 50%         |
| 0%              | 100%        |
> Assumption: 1 ARROW = 0.30 cents (USD) for this calculation.

### Calculating ARROW token amounts
Applications are incentivized to receive ARROW token using a multiplier. A **1.5x** multiplier is applied when calculating ARROW token amounts. 

**Example:** 
1. Applicant requests a grant worth **$1000**, with a **80% USDC** + **20% ARROW** blend. 
2. The ARROW amount would be calculated as `1000 * 0.2` i.e. $200 of ARROW token.
3. If the assumption is that 1 ARROW = $0.30, then $200 of ARROW becomes `200 / 0.3` i.e.  **666 ARROW**
4. The multiplier is then applied to be calculated as 666 * 1.5 = 999 ARROW
2. Total amount of grant: $800 + 999 ARROW

## Commitment Track


### Commitment Track Applications
An Application Template SHALL be made publicly available for applicants. Applications SHALL be reviewed between the second and third sunday of the month. 

### GBC Review
The GBC SHALL review every application and respond in a timely manner to the applicant.

### Distribution
The Grants and Bounties Committee is responsible for distributing Time Commitment Grants for each pod directly to its recipients.

- The GBC SHOULD determine the period for payouts and nominate an to communicate this to each applicant.
- By default this is assumed to be monthly, but MAY be increased to ease administrative burden if needed.
- Grants SHOULD be paid out in a blend of Arrow Token and USD, selected by the recipient.
- Conversion from USD to dollar-stablecoin payout token SHOULD be priced 1:1.

## Rationale
A walled garden can arise with a continued reliance on commitment tracks. It can limit or even discourage outside participation, which is contrary to how we aim to achieve our mission.

Arrow may have outgrown it's initial reliance on commitment tracks.

Below are some summarized responses to questions raised during the drafting of this AIP.

### Why not just scrap commitment track entirely and go 100% bounties?
Dedicated members to Arrow deserve to be compensated for their commitment. It is important to have a core of people not be disadvantaged for committing their time and energy to Arrow. 

### Why is base compensation reduction ~50%
 Reductions to 25% (of current base compensation) and 75% (of current base compensation) were also discussed as options. The 25% option seemed too much of a drastic change. The 75% seemed too small of a change to effectively judge the push to bounty incentive.

Ultimately we won't get true feedback until we evaluate our working culture and the output of contributors in the months after the adjustment.

### What type of contributor is eligible for a Time Commitment Grant
Anyone can apply, but they'll need a minimum of three things;
- Respect, decency and engagement within our community.
- Demonstrate an enthusiasm and passion to contribute.
- Demonstrate their ability to problem-solve and collaborate

In addition, applicants must be available and ready to complete the tasks below
- Each of these will be taken into account by GBC when reviewing and scoring applications

### What responsibilities does a contributor on a Time Commitment Grant have?
Examples of tasks that commitment track members may perform regularly that are hard to define into bounties are:
- attending daily meetings
- researching solutions to daily problems
- updating documentation
- internal communication, feedback and comments
- contributing to AIP process
- devoting time to thinking about solutions to problems
- active listening within meetings and reading forums
- sharing expertise and experience in various fields
- strategic input
- fostering community
- ongoing outreach with like-minded communities
- sharing news and industry updates

### How will this proposal change Arrow? And over what time-frame?
- The effects of a reduction in Commitment track compensation should be evident immediately in the number of applications for the new time commitment grant format. It is anticipated that many of the current commitment track contributors will renew their application, but this is a best guess.

- The largest benefit is expected to come in the form of more bounty definitions, proposals and completions from core members. It is anticipated that less funds will be required for the 'commitment track' core contributions and that this surplus can be reallocated to grants and bounties with a robust application and review process (via the GBC).

- The application and review process via an entity (GBC) should inspire more quality/thoughtfulness in proposals, as there is a real possibility that poor submissions will not get accepted, resulting in less potential monetary reward for the contributor. 

- An increase in the number of bounties and grants should lead to a situation where projects can set budgets for grants in the anticipation that the community/outside entities have an appetite for completing them. Arrow can then function as an efficient capital allocation system to fund important work.

### Other anticipated benefits of this AIP?
- Outside funding will look to see success in the number of completed grants/bounties. It will be an indicator of the DAO's ability to meaningfully scale. For reasons outlined in this AIP, a Time Commitment Grant process can effectively cover core operations whilst also opening the door for true global cooperation via publicly available grants and bounties for specific tasks.
- This AIP will incentivize contributors to clearly define deliverables and milestones stimulates good personal habits of focus and time management.
- Arrow becomes an organization familiar with thinking about how to break their projects and tasks into smaller chunks.
- It should theoretically become easier to create bounties for non-core contributor members, which is one of the key ways Arrow can scale.
- Completion of bounties should improve Arrow's global documentation (as it can now be stipulated as a requisite for payment).

### Why change naming of 'commitment track' to 'Time Commitment grant'? 
- It is useful to think of Arrow's incentives in terms of grants and bounties. The term 'Commitment track' can be confusing in an environment that uses similar definitions for the meaning of 'grants'.

- A grant has to be applied for, reviewed on its merits and accepted on the condition that there will be a fulfillment of a series pre-defined tasks. This feels more in line with how we want this application to be thought about. Perhaps the term 'track' has connotations of entitlement which is a cultural element we seek to move away from. 

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

# AIP-005

---
AIP: 5
title: Task, Bounty & Grant Submission  
description: Introducing the work submission standards for better documentation and accountability.
author: alperenag (@alperenag)
discussions-to: <https://dao.arrowair.com/t/bounty-grant-submission-aip-aip-005/73/9>
status: Final
type: Standards
created: 2024-12-09
vote-to: https://snapshot.org/#/s:arrowair.eth/proposal/0x217eb277109f30fc2d5a3634bea6a239be6b4031e9bb5ceef020d7a781c1ab63
vote-date: 2025-01-07
vote-result: Passed
---

## Abstract

This AIP introduces the term "task," referring to parts of work completed under a time-commitment grant, distinct from bounties and grants, which are paid separately; as well as proposing a new, standardized process for all task, bounty and grant submissions within Arrow Air DAO to enhance transparency, organization, and accountability. The proposed process includes the mandatory use of an "Information Note" document, which will serve as a detailed and structured blueprint for each submission, outlining the project's objectives, deliverables, methodology, and results.

Additionally, the AIP introduces a structured folder system within the GitHub repository to systematically organize all submissions and associated deliverables according to their project and category, ensuring all documentation and outputs are easily accessible and well-maintained for future reference. This structured approach will improve the efficiency of locating, tracking, and reviewing past work, fostering a streamlined process for future iterations or improvements.

Furthermore, a Discourse forum will be integrated to provide a dedicated space for technical discussions and collaboration related to each bounty or grant. This forum will mirror the structure of the GitHub repository, allowing DAO members and contributors to engage in transparent, documented conversations and updates throughout the project’s lifecycle. 


## Motivation

The current process for bounty and grant submissions within Arrow Air DAO lacks a standardized approach, resulting in several issues:
- **Inconsistent Documentation**: Submissions often vary in format and completeness, leading to difficulties in evaluating and validating work. A standardized template will address this inconsistency.
- **Lack of Traceability**: Without a structured system, it is challenging to track the history of projects, including decisions made and changes implemented. This makes it difficult to understand past work and its implications for ongoing or future projects.
- **Inefficient Evaluations**: The GBC (Grants and Bounties Council) faces challenges when assessing submissions due to the absence of a unified documentation format. By standardizing this process, evaluations will become more efficient and consistent.
- **Fragmented Communication**: Technical discussions and progress updates are often scattered across different platforms without sufficient structure. This fragmentation reduces collaboration efficiency and increases the risk of miscommunication.
- **Knowledge Loss**: Without a cohesive system for documenting project outcomes and discussions, valuable insights and lessons learned are not consistently captured or transferred within the organization.
- **Disorganized Repositories**: The lack of a uniform structure in repositories leads to difficulties in locating and referencing project-related documents, increasing the time and effort required for accessing information.
- **Untracked Contributions**: Tasks completed within time-commitment grants often go undocumented when they are not associated with a bounty or grant. This results in a loss of valuable information, insights, and progress made during the study period.

By implementing this AIP, the DAO aims to resolve:

- **Organized Access and Record-Keeping:** This system ensures that all designs, deliverables, documents, and discussions are accessible in a structured manner. If a specific design or discussion is needed in the future, it can be easily located in its corresponding folder or forum.
- **Justification and Documentation:** The Information Note provides justification for the work performed. It documents the reasoning behind the chosen approach, potential limitations, and areas that may have been overlooked, assisting in refining requirements.
- **Clear Evaluation Process for GBC:** The structure aids the GBC in evaluating the completion of bounties. GBC members will have a clear, documented basis to assess whether the task has been completed according to the outlined specifications and deliverables.
- **Accountability and Traceability:** By logging all deliverables and decisions across GitHub and Discourse, the system ensures that individuals or teams responsible for the work are held accountable. All progress and outcomes will be transparently recorded, ensuring visibility for search engines.
- **Knowledge Transfer and Know-How Development:** Consistent documentation of bounties/grants facilitates the evolution of know-how. Anyone can access past Information Notes and forum discussions to learn about completed tasks, understand what was attempted, and identify areas for improvement. This will create a valuable knowledge base for future work.
- **Comprehensive Documentation for General Documents:** This system ensures that all work done within the DAO is thoroughly documented. These records can be utilized when generating overarching or general documents, ensuring that all relevant details and designs are consistently referenced and integrated.
- **Task Documentation Framework**: Introducing the tasks ensures that the studies conducted within time commitment grant are also documented properly.


## Specification
1. **Definition of Task**:
   - A "task" **SHALL** refer to a specific part of work completed under a time-commitment grant.
   - Tasks **MUST NOT** be independently funded or paid separately, as they are considered contributions completed within the broader scope of a time-based commitment.
   - It **SHALL** be at the discretion of the project team to determine whether a specific work package qualifies as a task.
   - The completion of a task **SHALL** be determined by the project team.

2. **Discourse Topic Integration**:  
   - For each approved bounty or grant, a corresponding Discourse topic **MUST** be set up, mirroring the GitHub folder hierarchy for consistency (see Specifications #3). This integration ensures that all technical discussions, progress updates, and collaborative efforts are easy-to-find and accessible. 
   - The GBC **MUST** create the aforementioned Discourse topic and provide the link to the bounty/grant worker.
   - Each topic **SHALL** use proper tags for the bounty or grant.
   - All communication related to the bounty or grant **SHOULD** be documented in the topic, providing a transparent and traceable record of the project’s progress and discussions.

3. **Structured Folder System**:  
   - Each task, bounty or grant **MUST** have a dedicated folder within the GitHub repository. An example for the current Project Feather Pod follows this hierarchical structure:  
     `Project (e.g., project-feather) / task-bounty-grant / Prototype Number (e.g., PT3) / Discipline (e.g., Avionics) / Title (landing-gear)`
   - The folder **MUST** be named with the format that follows: ID - Title of the Task/Bounty/Grant
     - ID count is shared between tasks, bounties and grants. It does not indicate if the work is completed through a task, a bounty or a grant.
     - ID count **MUST** be zero-padded to maintain a total length of 4 digits. (For example: `0001`, `0002`, `0003`)
     - ID count **MUST** start from `0001` for each new project.
   - For each bounty or grant, the GBC **MUST** create the aforementioned folder and provide the link to the bounty/grant worker.
   - For each task, the task completer **MUST** create the aforementioned folder.
   - The Information Note (see Specifications #4) **MUST** be located in the designated folder.
   - All deliverables **SHALL** be located in the designated folder.
     - All pictures **MUST** be placed in a folder named "picture", under the designated folder. This will help viewing other main deliverables easily.  
     - If uploading the deliverable to the designated folder is not possible or convenient, this **MUST** be stated in the "Results and Deliverables" section of the Information Note, also adding the location of the deliverable. 
   - This structure guarantees that every submission is organized in a consistent manner, making it easy for contributors and reviewers to access and evaluate the information.

4. **Information Note Requirement**:  
   - The Information Note will be used as the primary document for the GBC to review and validate the submission. Without a complete and thorough Information Note, including the referenced bounty or grant proposal, the submission **MUST** be marked as incomplete and returned to the applicant for revisions.
   - Each task, bounty and grant submission **MUST** include an "Information Note" document, providing a structured and comprehensive overview of the project.
   - For each bounty or grant, the GBC **MUST** create the aforementioned Information Note template for the bounty/grant and provide the link to the bounty/grant worker. The template **MUST** include the **Bounty or Grant Proposal Document** section.
   - For each task, the task completer **MUST** create the aforementioned folder.
   - After approval of completion by the GBC, the Information Note **SHALL NOT** be modified, excluding the status section.
   - In case the bounty/grant involves milestones, the Information Note **MUST** be updated for the approval of each milestone.
   - The Information Note **MUST** contain the following sections:
     - **Status Section:**  
       The Information Note will begin with a **Status Section** that indicates whether the work is valid, superseded, or if the current work is overwriting another. This provides immediate clarity on the document's relevance. Three main blanks are to be filled:
       - Validity: 
         - If the work is valid:  
         `Validity: Valid`
         - If the work is conditionally valid:  
         `Validity: Valid for XXX`
         - If the work is invalid:  
         `Validity: Invalid`
       - Revision History:
         - If the work has not been superseded:  
         `Revision History: None`
         - If the work has been superseded:  
         `Revision History: Superseded by Bounty or Grant #*****` (including a link to the repository of the superseding work)
       - Replacement Log:
         - If the work has not been overwritten:  
         `Replacement Log: None`
         - If the work has been overwritten:  
         `Replacement Log: Overwrites Bounty or Grant #*****` (including a link to the repository of the overwritten work)
       - Reference Log:
         - If the work does not have a reference work completed before through a task, bounty or grant but does not overwrite it:  
         `Reference: None`
         - If the work has a reference work completed before through a task, bounty or grant but does not overwrite it:  
         `Reference: Bounty or Grant #*****` (including a link to the repository of the reference work)
       - Milestone Log:
         - If the work has milestones:
         `Latest Milestone: #` 
     - **Project Description:** A detailed explanation of the project, including the title, objectives, and the problem it addresses.
     - **Bounty or Grant Proposal Document:** This section will be a direct copy of the bounty or grant proposal document. It serves as a reference to the original proposal, ensuring all related information is easily accessible within the Information Note.
     - **Methodology:** This section outlines the approach chosen to address the project’s objectives. It includes the theoretical framework and underlying principles that guide the work, ensuring the methodology is grounded in relevant science, engineering, or best practices. The strategy defines the steps and sequence of activities, considering key factors such as feasibility, efficiency, and compatibility with existing systems. Limitations and constraints are acknowledged to provide a realistic understanding of the project's scope and challenges. The section also highlights important considerations like material requirements, sustainability, and the expertise needed to successfully execute the project.
     - **Results and Deliverables:** This section provides a comprehensive overview of all outputs expected from the task, applicable across various domains such as design, development, analysis, and testing. It includes references to all deliverables stored in the submission folder, ensuring complete and organized documentation of the project. Deliverables may consist of CAD models, blueprints, or schematics for physical components; software features or modules developed for system integration; and test results validating the performance and reliability of the solution. It may also cover material selection reports, manufacturing guides with production steps, and simulation or analysis data demonstrating feasibility. Additionally, cost estimation, efficiency assessments, and rationale for key decisions offer transparency and justification for the chosen approaches. This section ensures that all engineering deliverables are clearly documented, consistent with the submission folder’s contents, and accessible for future reference.
     - **Remarks:** This section provides an assessment of the work completed and offers insights for future considerations. It includes an evaluation of the outcomes, highlighting successes and any areas where the work met or exceeded expectations. It also discusses potential risks encountered during the project and the risks associated with using or implementing the work, offering strategies for managing or mitigating these risks. Additionally, possible improvements and suggestions for refining the approach or outcomes are provided. Recommendations for future or follow-up work may be outlined, offering guidance for further developments, iterations, or related projects that build upon the current task. This section ensures a reflective, comprehensive, and forward-looking perspective on the work completed, promoting continuous improvement and innovation.

![flowchart](../assets/aip-005/flow_chart.png)

## Rationale

This AIP is designed to bring consistency, transparency, and accountability to the Arrow Air DAO’s bounty and grant submission process. By implementing a structured template and folder system, the DAO will ensure that all submissions are evaluated based on standardized criteria. The Discourse integration will centralize communications, allowing all technical discussions to be archived and accessed easily. Alternate methods, such as unstructured documents or using only GitHub issues, were considered but found inadequate for maintaining long-term clarity and traceability.

## Backwards Compatibility

This AIP introduces a new requirement for future submissions and does not affect existing standards. All previous submissions are unaffected; however, retroactive compliance **MAY** be recommended for consistency. This ensures that all ongoing and future projects align with the new structured approach, but no incompatibilities arise from this change.

## Test Cases

Test cases for this AIP will include simulated scenarios where the GBC reviews different variations of the Information Note template to verify completeness and effectiveness. These tests will ensure that the template captures all required information and that the folder structure and Discourse integration function as intended, supporting efficient review and traceability.

## Reference Implementation

Currently, although no complete reference implementation is provided as this AIP primarily focuses on standardizing documentation and processes, an example Information Note has been prepared based on a previous task, the testbed landing gear design, to illustrate the intended structure and content.
[Information Note](../assets/aip-005/0001-landing-gear.md)

As this standard is adopted and used, more examples will accumulate, further enriching the repository of best practices and references.


## Security Considerations

This AIP does not introduce any new security vulnerabilities. However, it emphasizes the importance of maintaining the integrity of information stored and shared on the Discourse forum and GitHub repository. Proper permissions and access controls **MUST** be enforced to prevent unauthorized access and modification of documents, ensuring that the information remains secure throughout the submission and review process.

# AIP-006

---
AIP: 6
title: Create Projects Framework
description: Establish a framework to create and manage projects within the DAO
author: Thomas Garrison ([@thomasgarrison](https://github.com/thomasgarrison))
discussions-to: https://dao.arrowair.com/t/aip-006-discussion-framework-for-projects/97
status: Final
type: operational
created: 2024-12-08
vote-to: https://snapshot.box/#/s:arrowair.eth/proposal/0xfc2dded7be0c2dbabb498c91ec827c4877fddde9fb253871af983749aceb12de
vote-date: 2025-02-21
vote-result: Passed
---

## Abstract

This AIP proposes a framework for managing projects within the Arrow DAO. It defines what a project is, outlines the proposal process, establishes requirements for project leads, and defines the lifecycle of a project.

## Motivation

<!---
The motivation section should describe the "why" of this AIP. What problem does it solve? Why should someone want to implement this standard? What benefit does it provide to the Arrow ecosystem? What use cases does this AIP address?
-->

As the Arrow DAO continues to grow and evolve, it's essential to establish a clear and structured approach to project management. The community recognizes the need for clarity and accountability in project selection and execution. By establishing a well-defined project management process, the DAO can confidently add more projects in the future, knowing that each project has a clear direction, defined goals, and a responsible leader.

Historically, the DAO's project funding proposals have been approved with minimal review and rigor, lacking strong accountability. Additionally, there has been confusion around the concept of "pods", which has led to unclear expectations and inefficient resource allocation. This AIP aims to replace the current ad-hoc approach to project management with a well-defined framework for "projects", providing a clear understanding of what a project is, how it is proposed, and how it is managed. This, in turn, will enable the DAO to scale more efficiently and effectively.

With the shift towards using more grants and bounties, and the expansion of the DAO's focus beyond Feather, there is a growing desire to empower individuals to lead their own projects and grants. A well-defined project management process will enable project leaders to take ownership of their work, make decisions autonomously, and diligently drive their projects forward.

## Specification

### Defining a Project

A project in Arrow is a specific area of focus that clearly advances the goals and interests of the DAO as specified in AIP-008. Projects receive funding from the DAO treasury and are ultimately subject to the will of our entire community through DAO governance.

Projects in Arrow MUST have a specified leader. This can be a single person or a small group. That leader is responsible for managing the ongoing progress towards the project's area of focus on a regular basis. It is important to note that while projects do have leaders and certain deliverables to the DAO, this AIP does not specify any particular working group structure or organizational hierarchy for the contributors to any project. Beyond the requirement for a project leader, a project can take whatever organizational form the leader best thinks will serve its purpose. Projects may work best when the lead holds minimal discussions and meetings for the project as a whole and instead delegates that level of work to smaller working groups (pods/guilds) via grants and bounties.

### Documentation for Projects

A list of active and historical projects in Arrow SHALL be maintained in a public document (see AIP-007). For each project listed, this document MUST contain the following:

- A brief description of the project's goal and scope.

- The name of the project's leader(s).

- The current status of the project: [ACTIVE, STALE, COMPLETE, CANCELLED]

- A monthly spending cap for the project.

- The project’s start date

- An expiration date for the project's funding. (A template will be provided in AIP-007) Any amendments to AIP-007 MUST happen through DAO governance.

- A link to the project’s main repository

Each active project in Arrow MUST maintain a Github repository containing the project’s documentation, information notes and, when practical, the project’s outputs (technical data, 3D files, code, etc.). This repository SHALL serve as the top-level resource for all information regarding the project.

### Project Creation Process

Before being created, projects in Arrow must go through a formal vetting and approval process with the DAO governance. Committed support from the DAO at the beginning will allow projects to confidently proceed independently in their goals knowing that they already have the support of the DAO.

For someone with a project idea, the first step towards starting a new project in Arrow SHOULD be to informally vet the idea through discussions on Discord and our community calls. If the feedback seems good, then the project proposer can move forward more formally by posting the project idea on the DAO forum.

All project proposals MUST be discussed on the DAO forum prior to beginning the project or adding it to AIP-007. On the forum, the DAO SHALL discuss the project’s scope, alignment with AIP-008, budget, and timeline. Each project MUST be unique and SHOULD NOT fit within the scope of another project.

The final step to start the project is to approve an amendment to AIP-007 on Snapshot with the new project’s details. When this happens, the project is officially started.

### Project Leader Responsibilities

The project leader is the ultimate authority in managing the project in a manner to ensure that progress is being made towards the project's stated purpose. They are responsible for making project management decisions and MUST work with the GBC to issue grants and bounties for the work that the project requires. The project leader has the authority to make engineering design decisions for the project when there is disagreement. The project leader SHALL sufficiently delegate work to working groups, pods, and individuals such that the project isn’t overburdened with meetings.

The project leader MUST maintain the project in a well documented and organized state such that another leader could take over the project with minimal friction.

The project leader MUST manage the project’s budget such that the cap is not exceeded. The project leader may request an increase in the budget cap or an extension of the project’s funding when prudent by proposing an amendment to AIP-007.

Each month, the project leader MUST provide a narrative update on the project’s progress via a post to the DAO governance forum. The post SHALL be accompanied by an informal sentiment poll to gauge if the DAO is satisfied with the current progress and state of the project. A negative sentiment poll serves as feedback to the project leader to consider changing the way the project is managed, and it serves as feedback to the DAO to consider terminating the project or changing the project’s leader.

### Finances

Each project has a monthly budget cap and expiration date specified in AIP-007. At the start of each month, the DAO treasury SHALL provide the funds to each project’s wallet to bring it’s balance to the budget cap. Unspent funds each month SHALL NOT “roll over” so that the project wallet gets a balance higher than the specified cap. The DAO treasury MUST abide by the expiration dates in AIP-007 and MUST NOT fund projects beyond their expiration.

Each project’s wallet SHALL be a multisig with seats held by both the project leader and the GBC. The DAO Treasury multisig MAY hold a seat on the project multisig as an additional backup in case of lost keys or other failure by the other signers.

The project leader SHALL work with the GBC to appropriately coordinate the project’s tasks via grants and bounties. The GBC will serve as a supporter and champion for coordination while the project lead manages the project’s work and tasks.

The project leader is generally responsible for managing the project’s budget. The project leader SHALL process necessary reimbursements and other appropriate payments in a timely manner. The project leader may issue time commitment grants and other payments as they best see fit to accomplish the goals of the project.

### Replacing a Project Leader

A project’s leader may be changed at any time by amending AIP-007 via a proposal on Snapshot. This may happen if the DAO governance has lost faith in the current project leader or if the current project leader is unable or unwilling to continue managing the project.

If a project leader is ready to step down from their role as leader, they should consider their final duty to be finding and onboarding their replacement.

### Terminating a Project

A project may be terminated at any time by a ratified Snapshot proposal amending AIP-007 to update the project’s status to CANCELLED. This status overrides and cancels any previously approved funding for the project. If a project leader believes that the project is no longer serving the purposes of the DAO, they have the authority to cancel their project without going through DAO governance by notifying the DAO via the governance forum.

By default, projects will end when their funding expiration date is reached without any amendment to AIP-007 extending the expiration. When this happens, the AIP editors may update the project’s status in AIP-007 to STALE without a formal amendment via Snapshot.

Project leaders may also gracefully terminate their project upon completion of all of the stated project objectives by notifying the DAO on the governance forum. With a sentiment poll in agreement, the AIP editors may update the project’s status on AIP-007 to COMPLETE without a formal amendment via Snapshot.

##### Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

# AIP-007

---
AIP: 7
title: Create Projects List
description: Proposal to create a maintainable list of current and historical projects
author: Thomas Garrison (@thomasgarrison)
discussions-to: 
status: Living
type: informational
created: 2024-12-19
vote-to: https://snapshot.box/#/s:arrowair.eth/proposal/0x2e78c8a6b993c5087fe265abe74a16a330d89b1f8ac68be4af4c031fcb703523
vote-date: 2025-02-21
vote-result: Passed
---

## Abstract

This informational AIP lists active and historical projects within Arrow DAO, along with a description, named leader, and funding information for each of them as required by AIP-006.

## Motivation

Paired with AIP-006, this AIP will allow the Arrow community to keep track of and govern over projects within the DAO. This list will serve as a single source of truth for project and their statuses.

## Projects

| Date Started | Project Leader | Primary Goal/Scope                                                                                                                               | Status | Monthly Spending Cap | Funding Expiration | Main Repository                       |
| ------------ | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------ | -------------------- | ------------------ | ------------------------------------- |
| 2024-11-01   | Arrow Person   | This project exists to serve as an example for future projects, but it doesn't do any actual work beyond demonstrating the format of this table. | ACTIVE | 100 USDC, 20 ARROW   | 2025-03-31         | https://github.com/Arrow-air/dao-aips |

# AIP-008

---
AIP: 8
title: Mission and Broad Roadmap
description: Outlines the purpose and mission of Arrow, and creates a broad roadmap for the next few years.
author: Thomas Garrison ([@thomasgarrison](https://github.com/thomasgarrison))
discussions-to:
status: Final
type: operational
created: 2025-03-17
vote-to: https://snapshot.box/#/s:arrowair.eth/proposal/0xa7e3820cf365d9ab0210d3928b950742b56a8968ed5f342e403ec0314917f46c
vote-date: 2025-04-22
vote-result: Passed
---

## Abstract

This AIP expands on the overall purpose and mission of Arrow, then outlines a high-level explanation on how we will fulfill our mission and what the next few years of product development will look like.

## Specification

The purpose of our organization is to **increase physical connectedness to the people and places you love.** For us, this means anything that will make it easier, faster, or more affordable for people to travel to be with their friends, family, and communities. It also means creating ways for people to live where they want and retain a strong connection to the world around them.

Arrow aims to build purpose-aligned products by fostering a passionate, internet-native organization for anyone and everyone eager to build a more connected world. Through this, we can harness the collective abilities of our community through **unparalleled remote collaboration.**

Arrow conducts all of its work as openly as practical. Anyone in the world who shares our vision can join in and contribute with minimal friction, as long as doing so doesn’t compromise our rate of progress.

The best way Arrow can accomplish this purpose is by adding another layer of transportation infrastructure to fill in existing gaps or shortcomings within the current global network. This new layer of infrastructure will be VTOL aircraft that can transport people and goods, point to point regionally and locally with speed.
<br/>
<br/>


We see a series of stepping stones necessary for us to advance our organization as we pursue our purpose. Each step will build more experience, revenue, and confidence for us as we expand our efforts on the following steps.

We will begin by building and selling small multipurpose drones. This will allow us to demonstrate organizational competence with a project of moderate complexity. We’ll have a chance to find the best methods of remote collaboration while the stakes are lower. We will also get experience in shipping a refined product to customers, with the revenue flowing back to Arrow.

Once those multipurpose drones are refined and flying regularly in the real world, we will seek to certify them for commercial cargo use. This will be Arrow’s first experience interfacing with airspace regulators to bring an aircraft through certification. We will also gain additional revenue and experience running small cargo delivery logistics.

After that, we will build and certify a much larger drone. With a strong foundation from building smaller drones, Arrow will be well prepared to step into a project of much higher complexity and expand our experience with larger systems. This drone can be used to expand our cargo delivery platform as well as other multipurpose uses.

Next, with all of our experience in building and certifying large drones, Arrow will build our first manned aircraft product for general aviation. We’ll target an aircraft with two or four seats to be certified as a light-sport aircraft under the FAA’s MOSAIC rules. This will allow our aircraft to be available to a large number of sport pilots with less training required than other aircraft.

After we’ve delivered our first manned aircraft, we will shift focus towards building an aircraft and platform for air-taxi use. This will be the true mass-market solution that will allow non-pilots to travel with ease.
<br/>
<br/>

In short:

Build small multipurpose drones\
Certify those drones for commercial package delivery\
Build and certify a bigger drone\
Build a manned aircraft\
Build air taxis


##### Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
