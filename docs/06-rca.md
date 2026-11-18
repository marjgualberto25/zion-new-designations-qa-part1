# Root Cause Analysis – DEF-001

[← Back to README](../README.md)

> Based on a real defect type from my work on an insurance account, anonymised and mapped to this portfolio's fictional channel, products and agents. Dates, counts and messages are illustrative.

## Summary

| Field | Detail |
|---|---|
| Defect ID | DEF-001 |
| Title | MP and EP missing from AdvantageLife Pro USD product setup in Production (System A / DMS) |
| Environment | Production |
| Detected | 2026-12-11, one day after go-live |
| Detected by | New Business Operations (proposal rejected in System B) |
| Severity / Priority | High / P1: new designations could not sell an in-scope product |
| Affected | Proposals under MP and EP agents for AdvantageLife Pro USD (illustrative: 3 proposals) |
| Not affected | JFA, FA, SFA (all products); MP and EP for Malaya PHP, Pangarap PHP and AdvantageLife Pro PHP |
| Status | Closed: fix verified in Production on 2026-12-11; preventive action in place |

## What happened

MP and EP went live in the Zion channel on 2026-12-10. On 2026-12-11, a new business officer reported that a proposal written by Agnes Flores (MP) for **AdvantageLife Pro USD** was rejected in System B with *"Agent is not authorised to sell this product."* The same agent could submit proposals for the other three products.

Checking Production DMS showed that MP and EP had product setup lines for Malaya PHP, Pangarap PHP and AdvantageLife Pro PHP, but **none for AdvantageLife Pro USD**. Production had 6 of the 8 required lines.

The setup was correct in SIT, and all Part 1 test cases (including TC-008, TC-009 and TC-017) had passed there. The gap existed only in Production.

## Timeline

| Date / time | Event |
|---|---|
| Before go-live | BA held a walkthrough with stakeholders and the Products team, presenting the setup checklist: designations, all 8 product lines, hierarchy records and effective dates |
| Before go-live | Setup completed and tested in SIT; all Part 1 test cases passed |
| 2026-12-09 | Products team entered the Production setup manually ahead of go-live |
| 2026-12-10 | Go-live: MP and EP effective from this issue date |
| 2026-12-11 09:40 | New Business Ops report a rejected AdvantageLife Pro USD proposal under an MP agent |
| 2026-12-11 10:15 | BA/QA confirm 2 of 8 product setup lines missing in Production DMS |
| 2026-12-11 11:30 | Products team add the missing lines; BA/QA verify in Production |
| 2026-12-11 14:00 | Affected proposals resubmitted and accepted |

## Root cause analysis (5 Whys)

| # | Why? | Answer |
|---|---|---|
| 1 | Why was the proposal rejected? | MP and EP had no product setup line for AdvantageLife Pro USD in Production DMS. |
| 2 | Why were the lines missing? | The Production setup was entered manually by the Products team, and the USD lines were skipped. |
| 3 | Why were they skipped? | Human error during manual entry. The USD lines were included in the setup checklist presented at the walkthrough, but were overlooked when the Production setup was entered. |
| 4 | Why wasn't this caught before go-live? | Testing covered SIT only. Nothing required anyone to check the Production configuration after it was entered. |
| 5 | Why was there no Production check? | The release process ended at "setup done". A complete setup checklist was provided and walked through before go-live, but nothing required the setup owner to verify Production against it and provide evidence before go-live. |

**Root cause:** a process gap. Manual Production configuration had **no post-implementation verification (PIV)**, so a missed setup line could reach go-live unnoticed.

**Contributing factors**
- Production setup is manual and separate from SIT setup, so a passing SIT test doesn't prove Production is right.
- One product split into two currency lines is easy to treat as a single item.
- The setup checklist was used for guidance but not as a sign-off control: completing the setup did not require ticking off each item or showing evidence.

## Resolution

### Immediate fix (corrective)
1. Products team added the missing lines in Production DMS:

   | Designation | Product | Effective From | Effective To |
   |---|---|---|---|
   | MP | AdvantageLife Pro USD | 2026-12-10 | (blank) |
   | EP | AdvantageLife Pro USD | 2026-12-10 | (blank) |

   Effective From was set to the original go-live date, so policies issued from 2026-12-10 qualify.
2. BA/QA checked all 8 MP and EP lines in Production against the [Test Data](02-test-data.md) list.
3. Rejected proposals were identified with New Business Ops and resubmitted successfully.
4. Agents and New Business Ops were told the issue was resolved.

### Preventive action
**Post-implementation verification (PIV) document for every Production configuration change**, owned by whoever performs the setup.

- A Word document with a **screenshot of every configured item** in Production.
- Each screenshot shows the **desktop date and time**, as evidence of when the setup was in place.
- Items are checked against the approved setup list from the requirements, not from memory.
- Reviewed by the BA/QA and signed off **before go-live is announced**.
- Stored with the release documents for audit.

See the [PIV template](07-piv-template.md).

### Follow-up actions

| # | Action | Owner | Status |
|---|---|---|---|
| 1 | Add missing Production setup lines | Products team | Done |
| 2 | Verify all 8 lines in Production | BA/QA | Done |
| 3 | Resubmit affected proposals | New Business Ops | Done |
| 4 | Introduce PIV as a required step for Production configuration | Products team lead / Release manager | Done |
| 5 | Add "PIV signed off" to the go-live checklist | Release manager | Done |
| 6 | Use the walkthrough setup checklist as the PIV checklist, so setup and verification follow the same list | BA / Products team | Done |

## Lessons learned

- **A passing SIT test doesn't prove Production is right** when the two are configured separately by hand.
- **A checklist only prevents errors when its completion is verified.** The walkthrough checklist was accurate; what was missing was a step to confirm Production matched it.
- **Manual setup needs an independent check.** Even with clear requirements and a walkthrough, human error is possible, so a second person should verify against evidence before go-live.
