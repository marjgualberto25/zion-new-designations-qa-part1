# Requirements Traceability Matrix

[← Back to README](../README.md)

**Coverage: 19 of 19 acceptance criteria covered by 46 test cases.**

| Story | AC ID | Acceptance criterion | Linked test cases | # TCs | Coverage |
|---|---|---|---|---|---|
| US-01 | AC-01.1 | In System A, MP (Managing Partner) and EP (Executive Partner) exist as designations under the Zion channel only. | TC-001, TC-002, TC-003 | 3 | Covered |
| US-01 | AC-01.2 | In System B, the designation configuration holds MP and EP with the same codes and descriptions as System A. | TC-004, TC-005 | 2 | Covered |
| US-01 | AC-01.3 | Existing designations JFA, FA and SFA keep their codes and descriptions in both systems (regression). | TC-006 | 1 | Covered |
| US-01 | AC-01.4 | Creating a designation with a code that already exists in Zion is rejected. | TC-007 | 1 | Covered |
| US-02 | AC-02.1 | In System A, MP and EP each have a product setup line for Malaya PHP, Pangarap PHP, AdvantageLife Pro PHP and AdvantageLife Pro USD, with Effective From 2026-12-10 and Effective To blank. | TC-008, TC-009, TC-010 | 3 | Covered |
| US-02 | AC-02.2 | A policy with an MP or EP agent and an issue date before 2026-12-10 is rejected; with an issue date on or after 2026-12-10 it is accepted. | TC-012, TC-013, TC-014, TC-015 | 4 | Covered |
| US-02 | AC-02.3 | Product setup for JFA, FA and SFA is unchanged, and their policies are not affected by the new effective date (regression). | TC-011, TC-016 | 2 | Covered |
| US-02 | AC-02.4 | MP and EP agents can select all four Zion product lines and cannot select any product outside them. | TC-017, TC-018 | 2 | Covered |
| US-03 | AC-03.1 | System A has hierarchy records 103 (SFA = Level 1, MP = Level 2) and 104 (MP = Level 1, EP = Level 2), displayed as SFA → MP and MP → EP. | TC-019, TC-020, TC-023 | 3 | Covered |
| US-03 | AC-03.2 | System A has record 105 with EP as Level 1 and Level 2 blank, marking EP as self-reporting. | TC-021 | 1 | Covered |
| US-03 | AC-03.3 | Existing records 101 (JFA → FA) and 102 (FA → SFA) are unchanged (regression). | TC-022 | 1 | Covered |
| US-04 | AC-04.1 | When a profile is saved, System A generates a unique agent code that cannot be edited. | TC-031 | 1 | Covered |
| US-04 | AC-04.2 | Profiles for Jane Santos (JFA), Charlie Hunt (FA), Neo Blake (SFA), Agnes Flores (MP) and Eric Torch (EP) are saved under Zion with active licences and a linear reporting chain. | TC-027, TC-028, TC-029, TC-030 | 4 | Covered |
| US-04 | AC-04.3 | Assigning an upline that is not the next higher designation (skipping a level or reporting downward) is rejected. | TC-032, TC-033, TC-034, TC-035 | 4 | Covered |
| US-04 | AC-04.4 | An EP profile is saved only with 'Self-reporting?' ticked and no upline; the tickbox cannot be used for other designations. | TC-024, TC-025, TC-026 | 3 | Covered |
| US-04 | AC-04.5 | Profiles with an expired licence (Paolo Reyes, MP; Liza Cruz, FA) are saved, and their licence status shows Expired. | TC-036, TC-037 | 2 | Covered |
| US-05 | AC-05.1 | Agents created in System A reach System B through the API; entering an agent code in a proposal displays that agent's name, and an unknown code shows an error. | TC-038, TC-039, TC-040, TC-041 | 4 | Covered |
| US-05 | AC-05.2 | A proposal with an active-licence agent, an allowed product and an issue date on or after 2026-12-10 can be submitted. | TC-042, TC-043, TC-044 | 3 | Covered |
| US-05 | AC-05.3 | A proposal with an expired-licence agent cannot be submitted and shows 'Agent License is expired'. | TC-045, TC-046 | 2 | Covered |

_Execution counts are live in the Excel version and update from the Status column._
