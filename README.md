# Agency Channel – New Agent Designations (Part 1: Configuration)

A QA package for adding two new agent designations to an agency channel: setup across a distribution management system and a policy admin system, hierarchy, agent profiles, and the API sync between them. Part 1 of a two-part series; Part 2 covers commission rates and overrides.

> Fictional insurer, products and agents created for portfolio purposes. No real company data is used.

## The change

The business wants two new designations, **MP (Managing Partner)** and **EP (Executive Partner)**, above SFA in the **Zion** agency channel.

```
Before:  JFA → FA → SFA
After:   JFA → FA → SFA → MP → EP (self-reporting)
```

| Item | Detail |
|---|---|
| System A | Distribution Management System (DMS): designations, product setup, hierarchy, agent profiles |
| System B | Policy admin / new business: designation config, proposals, issuance |
| Integration | Agent data passed from System A to System B via API |
| Products | Malaya PHP, Pangarap PHP, AdvantageLife Pro PHP, AdvantageLife Pro USD |
| Effective From | 2026-12-10 (policy issue date); Effective To open-ended |
| Hierarchy rule | Linear, no skipping; stored as pairwise records in System A |

## What's inside

| # | Document | What it covers |
|---|---|---|
| 1 | [Business Rules](docs/01-business-rules.md) | 17 business rules and test-design assumptions |
| 2 | [Test Data](docs/02-test-data.md) | Designations, 8 product setup lines, hierarchy records, 7 test agents |
| 3 | [User Stories & Acceptance Criteria](docs/03-user-stories.md) | 5 user stories, 19 acceptance criteria |
| 4 | [Test Cases](docs/04-test-cases.md) | 46 test cases across System A, System B and the API |
| 5 | [Traceability Matrix](docs/05-traceability-matrix.md) | AC → test case mapping, 100% coverage |
| – | [Excel workbook](excel/Zion_New_Designations_Part1_QA.xlsx) | Same package with execution tracking and live coverage counts |

## Test coverage at a glance

| User story | Focus | ACs | Test cases |
|---|---|---|---|
| US-01 | Designation setup | 4 | 7 |
| US-02 | Product setup & effective date | 4 | 11 |
| US-03 | Hierarchy setup | 3 | 5 |
| US-04 | Agent profiles | 5 | 14 |
| US-05 | System B sync & proposals | 3 | 9 |
| **Total** | | **19** | **46** |

By type: Positive 24, Negative 12, Regression 5, Boundary 5.

## Test design approach

- **Cross-system verification**: the same designation codes and descriptions checked in both systems, plus an API check that agents created in System A arrive intact in System B
- **Boundary testing on the effective date**: issue dates of 9 and 10 December 2026, with an existing-designation control case
- **Hierarchy rule testing**: skip-level and downward reporting cases around the new levels, plus the EP self-reporting rule
- **Regression**: existing designations, product setup lines and hierarchy records checked against a pre-deployment baseline
- **Negative testing**: duplicate codes, products outside the channel, unknown agent codes and expired licences
- **Reusable test data**: a full five-level agent chain that Part 2 uses for commission and override testing

## Author

**Marj Gualberto** – Business Analyst / QA with 7 years in insurance and financial services (policy issuance, underwriting, commissions, agent and channel configuration; credit decisioning and KYC).
