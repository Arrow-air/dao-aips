
---
AIP: 10
title: Tokenomics V1
description: Outlines the current token distribuition and future plans
author: Erick Perdomo
discussions-to: https://dao.arrowair.com/t/aip-010-discussion-tokenomics-v1/159
status: Draft
type: Protocol
created: 2026-20-04
vote-to: 
vote-date: 
vote-result: 
---


## TL;DR

Arrow has 76.5M $ARROW sitting in its treasury with no formal framework for how it gets used. AIP-009 just passed and introduces the first real token utility. The Quiver dev-kit is nearly ready to ship. This document will define what $ARROW actually does.

**What this document establishes:**

**1. Fixed supply, no new minting.** $ARROW is capped at 100,000,000 tokens for V1. All token deployment draws from the existing treasury. No dilution. Future minting requires its own governance AIP.

**2. $ARROW has three active jobs in 2026:**

- **Governance:** 1 $ARROW = 1 vote, token weighted decisions on Snapshot

- **Manufacturing bonds:** manufacturers post slashable $ARROW as collateral under AIP-009. The bond guarantees quality to customers. Slashed tokens compensate customers first, then are burned

- **Contributor compensation:** every grant includes ≥10% $ARROW with a 1.5× multiplier. A 2× multiplier for 100% $ARROW bounties activates once LP liquidity is sufficient

**3. The treasury deploys 2,000,000 $ARROW in Year 1**, authorized by governance vote:

- 1,500,000 $ARROW → GBC administered bounty pool (~125K/month)

- 500,000 $ARROW → manufacturing rewards seed pool for AIP-009 manufacturers

**4. Vertiport and aircraft operator staking** are designed and described but parameters are deferred to Phase 2. The MOSAIC eVTOL market isn't mature enough to set responsible numbers today.

**5. Liquidity is the prerequisite for everything.** The existing $ARROW-USDC pool on Uniswap V3 has ~$1,989 in it, which is too thin for contributors to meaningfully sell. Thomas will seed a deeper personal LP as a bridge. DAO owned LP expansion requires either a legal consultation with the Wyoming UNA attorney or a community vote to proceed with documented risk acceptance.

**What this is NOT:**

- $ARROW does not entitle holders to profit or dividends

- V1 does not mandate stream deprecation. That's up to project leads

- This is a design doc, not a binding AIP. Community sentiment first, then AIP-010

**Current treasury status (April 8, 2026):** ~$125K USDC liquid, 3.239 ETH (~$7K). Approved project budgets total up to **~$80K/month** in recurring USDC caps: Spearhead ($35K), Caribou ($30K), GBC ($6.3K), Quiver commitments ($8.8K), plus a one time ~$19.5K for Project Longshot Phase 1. At cap rate burn, the USDC runway is approximately **6 weeks**. Quiver dev-kit sales and manufacturing protocol revenue are the path to extending runway.

---

## 1. Purpose & Scope

### Why V1, Why Now

Arrow has operated for over three years without a unified tokenomics framework. That was acceptable during early contributor bootstrapping, but three converging events make a formal framework necessary today:

1. **[AIP-009](https://github.com/Arrow-air/dao-aips/blob/main/AIPs/AIP-009.md) is live.** The manufacturing protocol introduces the first protocol native token utility: slashable $ARROW bonds from manufacturers. Without a broader framework, this mechanic floats in isolation. There is no documented relationship between bonds, the treasury, and contributor compensation.

2. **The DAO is at a financial inflection point.** Thomas's $400K OTC investment (1,333,333 $ARROW @ $0.30, 1 year cliff) has been partially deployed on operations. ~$125K USDC remains as of April 8, 2026. Five active projects (Quiver, Caribou, Spearhead, GBC, and Longshot) now carry approved monthly caps totaling ~$80K/month, putting the runway at approximately **6 weeks** at full burn. Quiver dev kit sales, potential new investors, and LP deepening are the near term inflows. This window must be used to establish a liquid $ARROW market and generate protocol revenue before the USDC balance is depleted.

3. **The shift to bounty first work demands a token that means something.** AIP-004 mandates ≥10% $ARROW in all grants, and the DAO is actively moving toward deliverable based work. $ARROW compensation is only motivating if contributors trust there is a path to liquidity and utility.

### What V1 Covers

- Token overview and current distribution

- Governance utility (existing and planned)

- Manufacturing bonds (AIP-009 formalization)

- Contributor compensation model (bounty first, $ARROW vesting)

- Future staking: vertiport and aircraft operators

- Treasury deployment plan and annual deployment rate

- Legal considerations

### What Is Deferred to V2+

- Permissionless manufacturer onboarding

- Per flight network usage rewards / loyalty rebates

- Full on chain governance (replacing Snapshot and treasury multisig)

- Aircraft operator staking specifics

- Vertiport stake parameter specifics (requires MOSAIC eVTOL market research)

- Dilutive token minting / true inflation (requires separate governance AIP)

---

## 2. Token Overview

### Basic Parameters

| Parameter | Value |
|-----------|-------|
| Token name | Arrow Air |
| Ticker | $ARROW |
| Total supply | 100,000,000 $ARROW, fixed for V1 |
| Token standard | ERC-20 upgradeable proxy (EIP-1967) |
| L1 contract | `0x736609D310B5F925531B5ad895925CB0586F6241` |
| OP contract | `0x78b3C724A2F663D11373C4a1978689271895256f` |
| LlamaPay vesting (OP) | 94 contributor compensation contracts |
| Vyper vesting factory (OP) | `0xB93427b83573C8F27a08A909045c3e809610411a` (Snapshot voting weight) |
| Reference price | $0.30/$ARROW (Thomas OTC, Oct 2025) |

**V1 supply is fixed at 100,000,000 $ARROW. No new tokens will be minted under this framework.** All token deployment described in this document draws from the existing DAO treasury balance. Any future dilutive minting requires its own standalone governance AIP and is explicitly out of scope for V1.

### Current Distribution (April 8, 2026)

| Holder / Bucket | $ARROW | % of Supply | Notes |
|-----------------|--------|-------------|-------|
| DAO Treasury (L1 Gnosis Safe) | 76,482,678 | 76.48% | Primary reserve, undistributed |
| Thomas Garrison, personal wallets (OP) | ~10,666,783 | 10.67% | Founder allocation, 2 OP wallets |
| Thomas Garrison, OTC escrow (LlamaPay) | 1,333,333 | 1.33% | Locked until Nov 2026 (1yr cliff) |
| Contributors, personal wallets (OP) | ~7,928,000 | 7.93% | Claimed tokens held in contributor EOAs |
| Contributors, LlamaPay claimable | ~2,913,000 | 2.91% | Streams ended, pending claim by recipients |
| Contributors, LlamaPay active stream | ~190,000 | 0.19% | Active stream to Dec 2026 |
| DAO Treasury (OP Multisig) | 411,431 | 0.41% | Operational OP treasury |
| GBC Multisig (L1) | 19,272 | 0.02% | Funded via March/April GBC proposal, available for grants & bounties |
| Unidentified OP holders | ~7,493 | 0.007% | Unmapped wallets among 66 total OP holders |
| Quiver Wallet (L1 shared multisig) | ~0 | ~0% | Was 8,400 in March. Balance transferred out |
| Uniswap V3 $ARROW-USDC LP | 3,251.0 | 0.003% | Thin pool, created by Erick |
| Individual L1 holders | ~10,160 confirmed | ~0.010% | small balances + bghughes (~5K bridged L1 Jan 2026) |

The 23.48M $ARROW on Optimism breaks down across 66 distinct OP holders. Contributor vesting runs through **LlamaPay** (94 contracts for compensation streams) and a separate **Vyper vesting factory** (`0xB93427b83573C8F27a08A909045c3e809610411a`) used for Snapshot voting weight. The ~2.9M "claimable" bucket represents tokens fully earned by contributors but not yet withdrawn. GoodluckH (~884K), deetoo (~874K), and Owlot (~930K) hold the largest unclaimed positions. See `arrow-token-holders.md` for the full contributor breakdown.

### Treasury Liquid Holdings (April 8, 2026)

| Asset | Amount | USD Value |
|-------|--------|-----------|
| USDC | 125,222.18 | $125,222 |
| ETH | 3.239 | ~$7,046 |
| $ARROW | 76,482,678 | — |
| **Total liquid** | | **~$132,268** |

$ARROW is shown at $0 by on chain price feeds due to the thin LP. The $0.30 OTC reference price implies a treasury $ARROW value of ~$22.9M, but this is not realisable at current LP depth and should not be treated as liquid.

### Original Allocation vs Current Reality

The original allocation framework earmarked:

- 20%: early contributor allocations

- 20%: commitment track and Coordinape compensation

- 10%: future investors (subject to securities laws)

- **50%: "TBD / use in Arrow rideshare protocol"**

That 50% TBD block, now sitting largely undisturbed in the DAO treasury, is what this document begins to fill in. V1 tokenomics is the answer to what "rideshare protocol utility" means at Arrow's current stage of development and through the next several years.

---

## 3. Token Utility Pillars

### 3a. Governance

$ARROW functions as a governance token. Holders have no entitlement to profit or dividends. Value derives from the utility of governing the network.

**Current state:**

- 1 $ARROW = 1 vote on Snapshot (arrowair.eth)

- Major protocol decisions (AIP votes), treasury allocations, and project approvals require token weighted votes

**V1 continuity:**

- Token weighted voting remains the basis for all governance decisions

- The GBC (established by [AIP-002](AIP-002.md)) continues to administer grants and bounties under DAO oversight

- The Projects Framework ([AIP-006](AIP-006.md)) governs project funding and accountability

**Long term goal (V2+):**

- Migrate all governance on chain

- Eliminate Snapshot and the treasury multisig

- Pure on chain token weighted voting with no off chain intermediaries

### 3b. Manufacturing Bonds (AIP-009)

AIP-009 establishes the first protocol native use of $ARROW: slashable collateral bonds posted by manufacturers who sell Arrow products.

**How bonds work:**

1. A manufacturer applies to join the protocol. The DAO issues them a risk adjusted bond limit.

2. To fulfill an order, the manufacturer must have sufficient unbonded $ARROW available. Each catalog item specifies an $ARROW bond amount required per unit shipped (e.g., 5,000 $ARROW per Quiver drone unit).

3. When a manufacturer ships a unit, the corresponding $ARROW is "used" and locked on their bond for **28 days** while the customer receives and inspects the product.

4. After 28 days with no dispute, tokens unlock and are again available or withdrawable.

5. If the DAO upholds a customer dispute, it may **slash** a portion of the bond.

**Slashing destination (resolved):** Slashed tokens are used first to compensate the affected customer and make them whole. Any slashed tokens in excess of the compensation amount are **burned permanently**, reducing total supply. This keeps the incentive clean. The DAO does not financially benefit from slashing manufacturers. Burns from slashing make the fixed supply modestly deflationary over time.

**DAO commission:** The catalog specifies a per item commission percentage paid to the DAO treasury on each sale. Commission rates vary by Arrow's design investment. Rates are higher for proprietary designs like the Quiver drone and lower for commodity components.

**Manufacturer rewards:** Manufacturers earn additional $ARROW rewards on top of their stake, proportional to sales volume or DAO targeted incentives (e.g., rewarding in stock inventory for critical parts). These rewards are funded from the annual treasury deployment pool described in §4.

**Unstaking cooldown:** 28 days (aligns with the per unit lock period).

**Governance role:** The DAO maintains the catalog, adding, removing, and adjusting bond amounts and commission rates. The DAO also serves as final arbiter for customer disputes and manufacturer slashing events.

### 3c. Contributor Compensation

Arrow's compensation model is moving toward grants and bounties with clear deliverables. V1 tokenomics formalizes how $ARROW fits into that model while leaving structural decisions to project leads.

**Project lead autonomy:** Stream vs bounty structure is left to the discretion of each project lead under [AIP-006](AIP-006.md). V1 does not mandate stream deprecation. Project leads have staffing autonomy to propose whatever compensation structure best serves their project.

**$ARROW in compensation (per AIP-004):**

- Every grant/bounty MUST include ≥10% of value in $ARROW

- Applicants select a USD/$ARROW blend in 5% increments (10% $ARROW minimum, up to 100% $ARROW)

- $ARROW portion is priced at $0.30 with a **1.5× multiplier** applied to incentivize token acceptance

- Example: $1,000 grant at 20% $ARROW → $200 of $ARROW → 666 $ARROW at $0.30 → **999 $ARROW** issued (1.5× applied)

- Total grant: $800 USDC + 999 $ARROW

**Enhanced multiplier for 100% $ARROW bounties:** V1 introduces a **2× multiplier** for bounties denominated entirely in $ARROW, providing a stronger incentive for projects that want to go fully $ARROW first. This lever is activated by a governance vote **only once LP depth is sufficient to support meaningful contributor selling.** Activating the 2× multiplier before the LP can absorb sell pressure would harm contributors who need to convert to USDC for expenses. LP deepening (see §5) is the prerequisite.

**Vesting:** Contributor $ARROW is issued via the ArrowVestingFactory on Optimism, creating per contributor cloned vesting contracts. The multisig can cancel a vesting contract. Upon cancellation, vested tokens go to the contributor and unvested tokens return to the treasury.

**Bounty pool:** The GBC administers a monthly $ARROW bounty allocation sourced from the treasury deployment cap described in §4. The pool cap is approved by the DAO via the AIP-006/AIP-007 project budget framework.

**Purely bounty based project model:**

- Project leader proposes project via AIP-006/AIP-007 process

- Approved project receives a monthly USDC+$ARROW budget cap in a project multisig

- Leader issues all work as open bounties, with no mandatory streams or commitment tracks

- Project leader holds seats on the multisig alongside the GBC

### 3d. Vertiport Operator Staking (Phase 2, 2027+)

Once Arrow's manufacturing protocol is producing real hardware and the AIP-008 roadmap advances toward manned aircraft, the DAO will begin building its vertiport network. Vertiport operators will stake $ARROW to register on chain.

**Planned mechanics:**

- Operators post $ARROW stake to register a vertiport in the Arrow network

- Protocol fee discount uses an **exponential decay model**: more $ARROW staked → lower per flight protocol fee. Small rural operators stake less and pay a higher base fee rate. Large hub operators can justify larger stakes for meaningful discounts

- **Geographic incentive weighting:** Vertiport registration incentives are weighted toward underserved corridors identified by the DAO's heatmap analysis

- **Onboarding incentive budget:** Tapering $ARROW rewards for early vertiport operators, decaying with each additional registration in a given metro

- Operators receive $ARROW via vesting style contracts tied to compliant operation over time

- Poorly performing vertiports may face stake slashing via DAO arbitration

**Stake parameters deferred:** Specific minimum stake amounts are not set in V1. Vertiport operators are commercial entities operating MOSAIC certified eVTOL aircraft. It is a market that is actively evolving across Joby, Archer, and other players with FAA certification timelines that remain uncertain. Setting a USD floor or $ARROW floor today would be premature and potentially fiscally irresponsible. Stake parameters will be established in a dedicated Phase 2 AIP informed by real market data at the time.

**Anti-centralization design:** The exponential decay model and geographic weighting are explicitly designed to prevent mega-operators from dominating the network. Arrow's mission is a shared network of independent operators, not consolidation by airlines.

### 3e. Aircraft Operator Staking (Phase 2, 2027+)

As Arrow moves through the AIP-008 roadmap toward manned aircraft and eventually air taxis, aircraft operators will also engage with the $ARROW protocol:

- Operators register aircraft on chain. Stake is proportional to aircraft value and operational risk profile

- Maintenance compliance and uptime tracked on chain. The protocol can penalize noncompliant operators via stake reduction

- Specifics to be formalized in a future AIP once Arrow has aircraft approaching commercial certification

### 3f. Network Usage Rewards (Phase 3, 2028+)

- Per flight $ARROW rebates to early passengers and cargo customers

- Loyalty mechanic seeded from the treasury deployment pool at the time

- Designed to bootstrap network effects during the platform launch phase and tapered over time as organic demand matures

- Full design deferred until air taxi platform development begins

---

## 4. Treasury Deployment Rate

### No New Mints in V1

$ARROW has a fixed supply of 100,000,000 tokens. V1 does not authorize any new minting. All $ARROW deployed to bounty pools, manufacturer rewards, or operator incentives comes from the existing DAO treasury balance of 76,501,950 $ARROW.

Future dilutive minting, if ever needed, requires a standalone governance AIP with explicit community approval. This is a deliberate design choice: it protects existing holders from dilution, simplifies the legal picture, and forces the DAO to make a conscious, transparent decision if and when the treasury is meaningfully depleted.

### Annual Deployment Cap

The DAO authorizes an **annual $ARROW deployment cap** via governance vote each year. This is not automatic. The community must affirmatively approve how much $ARROW leaves the treasury and to which buckets. Any undeployed $ARROW simply remains in the treasury.

**Year 1 (2026) proposed cap: 2,000,000 $ARROW**

At the $0.30 reference price, this represents ~$600K of token value deployed, meaningful but not treasury depleting (2.6% of the treasury balance).

### Year 1 Bucket Allocation

| Bucket | Annual $ARROW | Notes |
|--------|-------------|-------|
| Contributor bounty pool | 1,500,000 | GBC administered, ~125K $ARROW/month available |
| Manufacturing rewards | 500,000 | Seed pool for AIP-009 bonded manufacturers, rewards proportional to sales volume |
| Operator incentives | 0 | Phase 2, vertiport/aircraft staking not yet live |
| **Total Year 1** | **2,000,000** | Governance vote required to authorize |

### Year 2+ Adjustment

Bucket allocations should be revisited annually alongside the deployment cap vote. As the manufacturing protocol matures and operator staking comes online, the operator incentives bucket activates and the bounty pool proportion may decrease. Governance adjusts the split each year based on what the protocol actually needs.

### What Deployment Is NOT

Treasury deployment does not exist to support speculation or create artificial token demand. Every $ARROW deployed funds a specific protocol actor taking real action: completing bounties, manufacturing products, or operating infrastructure. This principle should guide all future deployment allocation debates.

---

## 5. Treasury Deployment Plan

### Current State

The DAO treasury holds (as of April 8, 2026):

- **76,482,678 $ARROW**, our primary long term reserve

- **~$125,222 USDC**, operational liquid runway

- **3.239 ETH** (~$7,046)

Approved project budgets as of April 2026 total up to **~$80,105/month** in recurring USDC caps across five active projects:

| Project | Monthly USDC Cap | Notes |
|---------|-----------------|-------|
| Project Spearhead | $35,000 | $28K labor + $7K hardware, runs through March 2027 |
| Project Caribou | $30,000 | $25K labor + $5K hardware |
| Project Quiver | $8,760 | Commitment grants only, tech bounties from team wallet reserves |
| GBC | $6,345 | $3,845 time grants + $2,500 pool |
| **Recurring total** | **~$80,105** | Caps, actual spend typically lower |

In addition, **Project Longshot** (custom Li-ion battery pack) was approved with a one time Phase 1 cap of ~$19,500 USDC + 10,000 $ARROW, targeting a May 2026 prototype.

At cap rate burn, the USDC runway from the April 2026 balance is approximately **6 weeks**. Actual spend has historically run below cap, but the margin is narrow. Quiver dev kit sales, Thomas's continued involvement, and potential new investors represent near term inflows. The LP deepening and revenue timeline are now critical.

### Phase 1: Immediate Priorities (2026)

**1. LP Deepening**

An $ARROW-USDC pool on Uniswap V3 (Ethereum Mainnet) already exists, seeded as a proof of concept with ~$1,989 in liquidity (~3,284 $ARROW + ~$1,000 USDC). This is far too thin to support meaningful contributor selling or external buyers.

LP deepening is the prerequisite for $ARROW compensation to work. Until the pool can absorb sell pressure from contributors converting $ARROW to USDC for expenses, the multiplier incentives and bounty first model are theoretical.

**Near term: Thomas personal LP as the default**

- Thomas seeds a deeper LP position personally to support near term contributor liquidity and the Quiver mini AI agent project (a separate AIP-006 proposal)

- Thomas's personal LP is the default path for the foreseeable future. The DAO will not execute its own LP transactions until the prerequisites below are met

- Price discovery has already been established at ~$0.30

**Path to DAO owned LP expansion**

The DAO owned LP is the right long term structure. Fee revenue accrues to the treasury, liquidity is community controlled, and it cannot be pulled without a governance vote. Two paths exist to get there:

- **Path A: Legal consultation:** A named UNA board member consults with the Wyoming UNA counsel on a narrow question: does a DAO owned Uniswap LP create securities exposure for US based board members and signers given the DAO's UNA structure and globally distributed contributor base? A single written opinion on this specific question is meaningful protection and is the preferred path before any DAO treasury LP action.

- **Path B: Community vote to proceed without counsel:** The community may vote to proceed with a DAO owned LP without formal legal opinion, provided a transparent risk disclosure is attached to the proposal. That disclosure must document: the Wyoming UNA structure, a Howey test self assessment, the precedent of the existing thin LP (already created from a project sub wallet), and the globally distributed nature of token holders. This is a legitimate path but the risk is knowingly accepted by the community on the record.

**Prerequisite before any DAO treasury LP action:** Either Path A or Path B must be completed and documented. This requirement exists to protect both the DAO and its individual board members and signers from acting without due diligence on the record.

**2. USDC Operational Runway**

The DAO should not be forced to sell $ARROW into a thin LP to fund operations. With ~$125K USDC remaining and ~$80K/month in active project caps, maintaining USDC reserves is the top priority. Quiver dev kit sales and manufacturing commission revenue are the primary near term paths to extending the runway without relying on further OTC deals or $ARROW liquidation.

**3. Annual $ARROW Deployment Cap Vote**

Authorize the Year 1 deployment cap (2,000,000 $ARROW) and bucket allocation via governance vote. This establishes the formal bounty pool budget and manufacturing rewards pool.

### Phase 2: Medium Term (2027)

**Business Development Grants**

$ARROW grants to OEM partners, vertiport developers, and certifying bodies in exchange for protocol participation and open source alignment. As Arrow moves through the AIP-008 roadmap, bringing partners on chain early creates network effects.

**Project Funding**

Projects funded monthly per the AIP-006/AIP-007 framework. As manufacturing protocol commission revenue grows, USDC pressure on the treasury decreases.

**Operator incentives bucket activated**

Once vertiport staking is live, the annual deployment cap vote should reallocate $ARROW from the bounty pool surplus into the operator onboarding incentives bucket.

### Phase 3: Long Term (2028+)

- Treasury transitions from $ARROW heavy to a diversified portfolio of ETH, USDC, and $ARROW as the token becomes liquid and protocol revenue grows

- DAO executes treasury management strategy: rebalancing LP positions, allocating trading fee yield, funding Phase 3 air taxi infrastructure

---

## 6. Roadmap Phases

| Phase | Timeframe | Product Milestone | Token Mechanics Active |
|-------|-----------|-------------------|----------------------|
| **Phase 1** | 2026 | Manufacturing protocol live, Quiver dev kits shipping, bounty only projects operational, LP deepened | Manufacturing bonds (AIP-009), contributor vesting (ArrowVestingFactory), DAO owned LP, monthly bounty pool, 1.5× $ARROW multiplier |
| **Phase 2** | 2027+ | Cargo drone certification, larger drone development, test vertiport network | Vertiport operator staking, aircraft operator staking, operator vesting contracts, operator incentives bucket active, 2× multiplier for 100% $ARROW bounties (if LP sufficient) |
| **Phase 3** | 2028+ | Manned aircraft, early air taxi platform | Per flight network rewards, loyalty rebates, mature staking ecosystem, on chain governance |

### Key Phase 1 Unlocks

The following must happen in 2026 for V1 tokenomics to function:

- [ ] LP deepened to support contributor selling (Thomas personal LP as bridge, DAO LP pending legal)

- [ ] AIP-009 manufacturing protocol smart contracts deployed and audited

- [ ] Annual $ARROW deployment cap vote (2,000,000 $ARROW, Year 1 buckets)

- [ ] Monthly bounty pool cap established and communicated to GBC

- [ ] ArrowVestingFactory documented and accessible to new contributors

- [ ] First bonded manufacturer onboarded under AIP-009 (Julius / Quiver dev kit in Germany)

---

## 7. Legal Considerations

*This section documents known legal risks that Arrow DAO is carrying without formal outside counsel. The DAO has chosen to proceed based on its existing UNA structure, the utility token framing established since 2022, and the precedent set by prior governance decisions. This is not legal advice. These risks should be understood and accepted by the community before ratifying V1.*

**$ARROW as a utility token, not a security**

- $ARROW holders have no entitlement to profit, dividends, or distributions from Arrow DAO operations

- Token value derives from utility (governance, bonding, staking) and scarcity, not profit sharing

- The DAO explicitly does not operate vertiports, aircraft, or manufacturing directly. It is a protocol facilitator ([AIP-009](AIP-009.md))

- The fixed 100M supply and no mint V1 stance simplifies the picture relative to inflationary token models

- This framing is self asserted by the DAO and has not been validated by outside counsel

**UNA structure**

- Arrow DAO operates as an Unincorporated Nonprofit Association (UNA), providing liability protection for members

- The DAO's internet native, non operational stance (manufacturers and operators are independent actors) is central to this structure

- Thomas has stated a goal of further decentralizing governance over time to reduce reliance on any individual or multisig

**LP creation**

- Creating a DAO owned LP carries potential securities law implications that the DAO is not currently in a position to formally evaluate

- As a result, **Thomas seeding a personal LP as an individual investor is the default path for near term liquidity**. This is a separate matter from DAO treasury actions and carries less institutional risk

- DAO owned LP expansion remains a long term goal but will not be pursued until the DAO either obtains legal review or the community explicitly votes to proceed without it

**Contributor tax obligations**

- $ARROW received as compensation is taxable income at fair market value at time of receipt

- Contributors are responsible for their own tax obligations

- The 1.5× (and future 2×) $ARROW multiplier increases the nominal compensation value. Contributors should factor this into their tax planning

**On chain governance transition**

- Replacing the Snapshot + multisig model with on chain governance is a long term goal

- Until that transition, the multisig retains authority over treasury transactions. The community should have visibility into and approval of all deployments

---

## 8. Resolved Design Decisions

The following design questions were worked through during the V1 drafting process. Resolutions are recorded here for transparency and community review.

**1. Token supply model**

No new minting in V1. The 100,000,000 $ARROW supply is fixed. All token deployment draws from the existing treasury. Future dilutive minting requires a standalone governance AIP. *Rationale: avoids holder dilution, simplifies legal picture, keeps the DAO intentional about any future supply changes.*

**2. Slashing destination**

Slashed manufacturer bonds compensate the affected customer first. Any excess beyond full customer compensation is burned permanently. The DAO does not retain slashed tokens as revenue. *Rationale: keeps incentives clean. The DAO should not benefit financially from punishing manufacturers.*

**3. LP structure**

DAO owned LP (Uniswap V3, Ethereum Mainnet) is the long term target. An existing thin pool (~$1,989) is already live. Thomas seeds a deeper personal LP position as a bridge to support contributor liquidity and the Quiver mini project. DAO formally deepens its own position after legal review. *Rationale: DAO ownership ensures fee revenue accrues to treasury and liquidity is community controlled. Thomas's personal bridge avoids the DAO making the initial price decision before legal clears.*

**4. Vertiport stake parameters**

Specific stake amounts are deferred to a Phase 2 AIP. The MOSAIC eVTOL market, FAA certification timelines, and competitive landscape (Joby, Archer, etc.) are too uncertain to set responsible figures today. The staking *mechanism* (exponential decay fee model, geographic weighting, USD denominated floor converted at TWAP) is established in V1. The numbers come later. *Rationale: fiscal responsibility over false precision.*

**5. Commitment stream deprecation**

Not mandated by V1. Stream vs bounty structure is left to project lead discretion per AIP-006. V1 introduces the 2× multiplier for 100% $ARROW bounties as an opt in incentive toward $ARROW first projects, activated by governance vote once LP depth is sufficient. *Rationale: project lead staffing autonomy. Market incentives rather than mandates.*

**6. Annual treasury deployment rate and buckets**

Year 1 deployment cap: **2,000,000 $ARROW**, subject to governance vote. Buckets: 1,500,000 $ARROW to the contributor bounty pool, 500,000 $ARROW to the manufacturing rewards seed pool, 0 to operator incentives (Phase 2). Bucket allocations revisited annually. *Rationale: conservative deployment preserves treasury. Bounty pool is the only immediately active bucket in 2026. Operator incentives activate in Phase 2.*

---

## 9. Next Steps

1. **Share in Arrow DAO forum** for community discussion and sentiment poll

2. **LP deepening:** Thomas seeds personal LP position to support contributor liquidity and the Quiver mini project. DAO owned LP expansion is deferred until community votes to proceed or legal review becomes available

3. **Annual deployment cap vote:** governance proposal to authorize 2,000,000 $ARROW Year 1 deployment and bucket allocation

4. **GBC bounty pool communication:** formal monthly $ARROW cap to be communicated to GBC and added to AIP-007

5. **Julius and AIP-009 onboarding:** first manufacturer onboarded under manufacturing protocol, proof of concept for bond mechanics

6. **Formal AIP:** if community sentiment is positive, draft **AIP-010: Arrow Tokenomics V1**

---

## Appendix A: AIP Reference Map

| AIP | Title | Relevance to Tokenomics |
|-----|-------|------------------------|
| [AIP-001](AIP-001.md) | AIP Purpose and Guidelines | Defines the process this document must follow to become AIP-010 |
| [AIP-002](AIP-002.md) | Creation of Grants and Bounties Committee | GBC administers bounty pool and grant $ARROW disbursements |
| [AIP-004](AIP-004.md) | Introduce Time Commitment Grant | Defines minimum 10% $ARROW in compensation, 1.5× multiplier, $0.30 reference price |
| [AIP-006](AIP-006.md) | Create Projects Framework | Projects framework governs budget caps, multisigs, and project lead autonomy |
| [AIP-007](AIP-007.md) | Active Projects List | Canonical list of funded projects. Bounty pool cap to be added here |
| [AIP-008](AIP-008.md) | Mission and Broad Roadmap | Defines the product sequence (drones → cargo → manned aircraft → air taxis) that V1 phases map to |
| [AIP-009](AIP-009.md) | Manufacturing Protocol Basic Design | First live token utility: manufacturer bonds, slashing, DAO commission, rewards pool |

---

## Appendix B: Key Addresses

| Entity | Network | Address |
|--------|---------|---------|
| DAO Treasury (Gnosis Safe) | Ethereum Mainnet | `0x03b5dc2ce78a7bee9f66dd619b291595a2e166bb` |
| DAO OP Multisig | Optimism | `0xaDc17e5f0e9F755C717B2beE43B590260034b852` |
| Quiver Wallet (Gnosis Safe) | Ethereum Mainnet | `0x90f926BBfc8f0EB3Fb2a7237AD6d257EA4b75730` |
| $ARROW Token (L1) | Ethereum Mainnet | `0x736609D310B5F925531B5ad895925CB0586F6241` |
| $ARROW Token (OP) | Optimism | `0x78b3C724A2F663D11373C4a1978689271895256f` |
| Vyper Vesting Factory (Snapshot voting) | Optimism | `0xB93427b83573C8F27a08A909045c3e809610411a` |
| Uniswap V3 $ARROW-USDC LP | Ethereum Mainnet | `0x84c4d2339c03aE3F7D5B7e63e3477b1dCA1610Ec` |
| thomasg.eth (primary OP wallet) | Optimism | `0x76EF4B28df1F590db4cD680675d734c27CAa32BA` |
| Thomas OTC escrow (LlamaPay) | Optimism | `0x2b54223d67136b7c837607c6fe4488c7ceaa555d` |

---

## Appendix C: DAO Multisig Wallets

*USDC balances as of April 9, 2026.*

### DAO-Level

| Entity | Network | USDC Balance | Address |
|--------|---------|-------------|---------|
| DAO Treasury | Ethereum Mainnet | $125,222.18 | `0x03b5Dc2CE78a7bEe9F66DD619b291595a2E166BB` |
| DAO Sub Wallet | Ethereum Mainnet | $45.99 | `0xb9C3236971B24B5dCfa329a4207544b3fc2Ec3ee` |
| DAO (OP) | Optimism | $0 | `0xaDc17e5f0e9F755C717B2beE43B590260034b852` |
| GBC | Ethereum Mainnet | $5,000.00 | `0x7cFd3D29fD7b13CA33E49bA6b11b79bEF89e5906` |

### Projects

| Entity | Network | USDC Balance | Address |
|--------|---------|-------------|---------|
| Project Quiver | Ethereum Mainnet | $24,087.65 | `0x90f926BBfc8f0EB3Fb2a7237AD6d257EA4b75730` |
| Project Feather | Optimism | $1,209.18 | `0xb0aF25E6c000DC99CFD77E26baBCAC05C19666Ca` |
| Project Spearhead | Ethereum Mainnet | $27,918.62 | `0x1952FFc130AcC76C5a56c888d4Bc8D9385267272` |
| Project Caribou | Ethereum Mainnet | $30,000.00 | `0x5f38B14db41031290F6D482Db952FF06b3b2C536` |
| Project Onboarding | Ethereum Mainnet | $18,300.00 | `0xFA60Dd8E059505309a5fE9dd0fD6B6Bd373Ac597` |
| Project Visibility | Ethereum Mainnet | $1,095.21 | `0xE59972D693c3371528fc8D0120eF7299672D5212` |

### Inactive

| Entity | Network | USDC Balance | Address |
|--------|---------|-------------|---------|
| Growth | Ethereum Mainnet | $1,997.13 | `0x49300980960CBea125929e678343c36563AB48F0` |
| HW Engineering | Ethereum Mainnet | $7,073.23 | `0x79E56F5e632d4f47b07DccDeeB2cB46Faab7266D` |
| Services | Ethereum Mainnet | $3,506.65 | `0xd0589F42B577834A2E2812C272809f136880aD8F` |

**Total USDC across all DAO wallets: ~$245,456**

---

*Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).*
