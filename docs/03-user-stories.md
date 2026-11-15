# User Stories & Acceptance Criteria

[← Back to README](../README.md)

**Epic EP-ZDES-1:** Add MP and EP designations to the Zion agency channel (configuration). Part 1 of 2.

## US-01 · Designation setup

> As a distribution admin, I want MP and EP set up as designations in System A under Zion and in System B's configuration, so that both systems recognise the new ranks.

| AC ID | Acceptance criterion | Rule ref |
|---|---|---|
| AC-01.1 | In System A, MP (Managing Partner) and EP (Executive Partner) exist as designations under the Zion channel only. | BR-01 |
| AC-01.2 | In System B, the designation configuration holds MP and EP with the same codes and descriptions as System A. | BR-02 |
| AC-01.3 | Existing designations JFA, FA and SFA keep their codes and descriptions in both systems (regression). | BR-01–BR-02 |
| AC-01.4 | Creating a designation with a code that already exists in Zion is rejected. | BR-03 |

## US-02 · Product setup & effective date

> As a distribution admin, I want MP and EP added to the product setup of the four Zion product lines from 10 December 2026, so that the new ranks can sell the same products as JFA, FA and SFA.

| AC ID | Acceptance criterion | Rule ref |
|---|---|---|
| AC-02.1 | In System A, MP and EP each have a product setup line for Malaya PHP, Pangarap PHP, AdvantageLife Pro PHP and AdvantageLife Pro USD, with Effective From 2026-12-10 and Effective To blank. | BR-04–BR-05 |
| AC-02.2 | A policy with an MP or EP agent and an issue date before 2026-12-10 is rejected; with an issue date on or after 2026-12-10 it is accepted. | BR-05–BR-06 |
| AC-02.3 | Product setup for JFA, FA and SFA is unchanged, and their policies are not affected by the new effective date (regression). | BR-04 |
| AC-02.4 | MP and EP agents can select all four Zion product lines and cannot select any product outside them. | BR-07 |

## US-03 · Hierarchy setup

> As a distribution admin, I want the Zion hierarchy extended to SFA → MP → EP, so that reporting lines (and later overrides) follow the new ranks.

| AC ID | Acceptance criterion | Rule ref |
|---|---|---|
| AC-03.1 | System A has hierarchy records 103 (SFA = Level 1, MP = Level 2) and 104 (MP = Level 1, EP = Level 2), displayed as SFA → MP and MP → EP. | BR-08–BR-09 |
| AC-03.2 | System A has record 105 with EP as Level 1 and Level 2 blank, marking EP as self-reporting. | BR-10 |
| AC-03.3 | Existing records 101 (JFA → FA) and 102 (FA → SFA) are unchanged (regression). | BR-09 |

## US-04 · Agent profiles

> As a distribution admin, I want to create agent profiles for the new and existing designations in System A, so that a complete Zion reporting chain exists for selling and commission.

| AC ID | Acceptance criterion | Rule ref |
|---|---|---|
| AC-04.1 | When a profile is saved, System A generates a unique agent code that cannot be edited. | BR-11 |
| AC-04.2 | Profiles for Jane Santos (JFA), Charlie Hunt (FA), Neo Blake (SFA), Agnes Flores (MP) and Eric Torch (EP) are saved under Zion with active licences and a linear reporting chain. | BR-12 |
| AC-04.3 | Assigning an upline that is not the next higher designation (skipping a level or reporting downward) is rejected. | BR-12 |
| AC-04.4 | An EP profile is saved only with 'Self-reporting?' ticked and no upline; the tickbox cannot be used for other designations. | BR-10, BR-13 |
| AC-04.5 | Profiles with an expired licence (Paolo Reyes, MP; Liza Cruz, FA) are saved, and their licence status shows Expired. | BR-14 |

## US-05 · System B sync & proposals

> As a new business officer, I want agents created in System A to be available in System B proposals, so that policies can be written under the new designations.

| AC ID | Acceptance criterion | Rule ref |
|---|---|---|
| AC-05.1 | Agents created in System A reach System B through the API; entering an agent code in a proposal displays that agent's name, and an unknown code shows an error. | BR-15–BR-16 |
| AC-05.2 | A proposal with an active-licence agent, an allowed product and an issue date on or after 2026-12-10 can be submitted. | BR-05, BR-07 |
| AC-05.3 | A proposal with an expired-licence agent cannot be submitted and shows 'Agent License is expired'. | BR-17 |

---

**Out of scope:** basic commission rates and overrides (Part 2), licence renewal processing, agent termination, reports.
