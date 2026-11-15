# Test Cases – Part 1 Configuration

[← Back to README](../README.md)

Environment: SIT · Total: **46 test cases** · Status options: Not Run, Pass, Fail, Blocked

## Summary

| TC ID | AC ID | System | Scenario | Type | Priority | Status |
|---|---|---|---|---|---|---|
| TC-001 | AC-01.1 | A | Verify MP designation exists under Zion | Positive | High | Not Run |
| TC-002 | AC-01.1 | A | Verify EP designation exists under Zion | Positive | High | Not Run |
| TC-003 | AC-01.1 | A | MP and EP are not set up under other channels | Negative | Medium | Not Run |
| TC-004 | AC-01.2 | B | Verify MP in System B designation config | Positive | High | Not Run |
| TC-005 | AC-01.2 | B | Verify EP in System B designation config | Positive | High | Not Run |
| TC-006 | AC-01.3 | A & B | Existing designations unchanged in both systems | Regression | High | Not Run |
| TC-007 | AC-01.4 | A | Reject duplicate designation code | Negative | Medium | Not Run |
| TC-008 | AC-02.1 | A | MP product setup lines and dates | Positive | High | Not Run |
| TC-009 | AC-02.1 | A | EP product setup lines and dates | Positive | High | Not Run |
| TC-010 | AC-02.1 | A | Blank Effective To saves as open-ended | Boundary | Medium | Not Run |
| TC-011 | AC-02.3 | A | Existing designations' product setup unchanged | Regression | High | Not Run |
| TC-012 | AC-02.2 | B | Reject MP policy issued before effective date | Boundary | High | Not Run |
| TC-013 | AC-02.2 | B | Accept MP policy issued on effective date | Boundary | High | Not Run |
| TC-014 | AC-02.2 | B | Reject EP policy issued before effective date | Boundary | High | Not Run |
| TC-015 | AC-02.2 | B | Accept EP policy issued on effective date | Boundary | High | Not Run |
| TC-016 | AC-02.3 | B | Existing designation not affected by new effective date | Regression | High | Not Run |
| TC-017 | AC-02.4 | B | MP agent can select all four Zion products | Positive | High | Not Run |
| TC-018 | AC-02.4 | B | EP agent cannot select a non-Zion product | Negative | Medium | Not Run |
| TC-019 | AC-03.1 | A | Verify record 103 SFA → MP | Positive | High | Not Run |
| TC-020 | AC-03.1 | A | Verify record 104 MP → EP | Positive | High | Not Run |
| TC-021 | AC-03.2 | A | Verify record 105 EP self-reporting | Positive | High | Not Run |
| TC-022 | AC-03.3 | A | Existing records 101 and 102 unchanged | Regression | High | Not Run |
| TC-023 | AC-03.1 | A | Full Zion chain is continuous with no gaps | Positive | Medium | Not Run |
| TC-024 | AC-04.4 | A | Create EP agent with Self-reporting ticked | Positive | High | Not Run |
| TC-025 | AC-04.4 | A | Reject EP agent without Self-reporting and no upline | Negative | High | Not Run |
| TC-026 | AC-04.4 | A | Self-reporting not allowed for non-EP designation | Negative | High | Not Run |
| TC-027 | AC-04.2 | A | Create MP agent reporting to EP | Positive | High | Not Run |
| TC-028 | AC-04.2 | A | Create SFA agent reporting to MP | Positive | High | Not Run |
| TC-029 | AC-04.2 | A | Create FA agent reporting to SFA | Positive | High | Not Run |
| TC-030 | AC-04.2 | A | Create JFA agent reporting to FA | Positive | High | Not Run |
| TC-031 | AC-04.1 | A | Agent codes are generated, unique and read-only | Positive | High | Not Run |
| TC-032 | AC-04.3 | A | Reject JFA reporting directly to MP (skip) | Negative | High | Not Run |
| TC-033 | AC-04.3 | A | Reject FA reporting directly to EP (skip) | Negative | High | Not Run |
| TC-034 | AC-04.3 | A | Reject SFA reporting directly to EP (skip) | Negative | High | Not Run |
| TC-035 | AC-04.3 | A | Reject MP reporting to a lower designation | Negative | Medium | Not Run |
| TC-036 | AC-04.5 | A | Save MP agent with expired licence | Positive | High | Not Run |
| TC-037 | AC-04.5 | A | Save FA agent with expired licence | Positive | High | Not Run |
| TC-038 | AC-05.1 | A → B | All test agents reach System B via API | Positive | High | Not Run |
| TC-039 | AC-05.1 | B | Agent code shows MP agent name | Positive | High | Not Run |
| TC-040 | AC-05.1 | B | Agent code shows EP agent name | Positive | High | Not Run |
| TC-041 | AC-05.1 | B | Unknown agent code shows an error | Negative | Medium | Not Run |
| TC-042 | AC-05.2 | B | Submit proposal with MP agent | Positive | High | Not Run |
| TC-043 | AC-05.2 | B | Submit proposal with EP agent | Positive | High | Not Run |
| TC-044 | AC-05.2 | B | Submit proposal with existing-designation agent | Regression | Medium | Not Run |
| TC-045 | AC-05.3 | B | Block proposal for MP agent with expired licence | Negative | High | Not Run |
| TC-046 | AC-05.3 | B | Block proposal for FA agent with expired licence | Negative | High | Not Run |

## Detailed test cases

### US-01 · Designation setup

#### TC-001 – Verify MP designation exists under Zion

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.1 |
| System | A |
| Module | Designation |
| Type / Priority | Positive / High |
| Preconditions | MP deployed to SIT |
| Test data | Channel: Zion<br>Code: MP |

**Steps**

1. Log in to System A as distribution admin.
2. Go to Channel Setup > Zion > Designations.
3. Search 'MP'.

**Expected result:** MP is listed with description 'Managing Partner' under Zion.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-002 – Verify EP designation exists under Zion

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.1 |
| System | A |
| Module | Designation |
| Type / Priority | Positive / High |
| Preconditions | EP deployed to SIT |
| Test data | Channel: Zion<br>Code: EP |

**Steps**

1. Log in to System A.
2. Go to Channel Setup > Zion > Designations.
3. Search 'EP'.

**Expected result:** EP is listed with description 'Executive Partner' under Zion.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-003 – MP and EP are not set up under other channels

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.1 |
| System | A |
| Module | Designation |
| Type / Priority | Negative / Medium |
| Preconditions | At least one other channel exists in System A |
| Test data | Any non-Zion channel |

**Steps**

1. Open Designations for each non-Zion channel.
2. Search 'MP' and 'EP'.

**Expected result:** MP and EP do not appear under any channel except Zion.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-004 – Verify MP in System B designation config

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.2 |
| System | B |
| Module | Designation |
| Type / Priority | Positive / High |
| Preconditions | System B team has added the new designations |
| Test data | Code: MP |

**Steps**

1. Log in to System B as config user.
2. Go to Configuration > Agent Designations.
3. Search 'MP'.

**Expected result:** MP exists with description 'Managing Partner', matching System A exactly (code and text).

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-005 – Verify EP in System B designation config

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.2 |
| System | B |
| Module | Designation |
| Type / Priority | Positive / High |
| Preconditions | System B team has added the new designations |
| Test data | Code: EP |

**Steps**

1. Log in to System B.
2. Go to Configuration > Agent Designations.
3. Search 'EP'.

**Expected result:** EP exists with description 'Executive Partner', matching System A exactly (code and text).

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-006 – Existing designations unchanged in both systems

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.3 |
| System | A & B |
| Module | Designation |
| Type / Priority | Regression / High |
| Preconditions | Baseline of JFA, FA, SFA captured before deployment |
| Test data | JFA, FA, SFA |

**Steps**

1. Open designation lists in System A (Zion) and System B.
2. Compare JFA, FA, SFA against the baseline.

**Expected result:** JFA = Junior Financial Advisor, FA = Financial Advisor, SFA = Senior Financial Advisor in both systems; no other attribute changed.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-007 – Reject duplicate designation code

| Field | Detail |
|---|---|
| Story / AC | US-01 / AC-01.4 |
| System | A |
| Module | Designation |
| Type / Priority | Negative / Medium |
| Preconditions | MP already exists under Zion |
| Test data | New designation: Code MP, Description 'Managing Partner 2' |

**Steps**

1. Go to Zion > Designations > Add.
2. Enter test data.
3. Click Save.

**Expected result:** Save is blocked with a duplicate-code message, e.g. 'Designation code already exists in this channel'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

### US-02 · Product setup & effective date

#### TC-008 – MP product setup lines and dates

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.1 |
| System | A |
| Module | Product Setup |
| Type / Priority | Positive / High |
| Preconditions | MP exists under Zion |
| Test data | Designation: MP; 4 product lines |

**Steps**

1. Go to Product Setup > Zion.
2. Filter designation = MP.
3. Review each line.

**Expected result:** 4 lines exist (Malaya PHP, Pangarap PHP, AdvantageLife Pro PHP, AdvantageLife Pro USD); each has Effective From 2026-12-10 and Effective To blank.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-009 – EP product setup lines and dates

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.1 |
| System | A |
| Module | Product Setup |
| Type / Priority | Positive / High |
| Preconditions | EP exists under Zion |
| Test data | Designation: EP; 4 product lines |

**Steps**

1. Go to Product Setup > Zion.
2. Filter designation = EP.
3. Review each line.

**Expected result:** 4 lines exist for the same products; each has Effective From 2026-12-10 and Effective To blank.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-010 – Blank Effective To saves as open-ended

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.1 |
| System | A |
| Module | Product Setup |
| Type / Priority | Boundary / Medium |
| Preconditions | Product setup screen open |
| Test data | Designation: MP; Product: Malaya PHP; Effective To: blank |

**Steps**

1. Open the MP / Malaya PHP line.
2. Leave Effective To blank.
3. Click Save.

**Expected result:** Line saves with no validation error; Effective To shows blank (no end date).

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-011 – Existing designations' product setup unchanged

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.3 |
| System | A |
| Module | Product Setup |
| Type / Priority | Regression / High |
| Preconditions | Baseline of JFA, FA, SFA product setup captured |
| Test data | JFA, FA, SFA × 4 products |

**Steps**

1. Filter Product Setup by JFA, FA, SFA.
2. Compare with baseline.

**Expected result:** All 12 existing lines match the baseline, including their original effective dates.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-012 – Reject MP policy issued before effective date

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.2 |
| System | B |
| Module | Effective Date |
| Type / Priority | Boundary / High |
| Preconditions | Agnes Flores (MP) synced to System B |
| Test data | Agent: Agnes Flores (MP)<br>Product: Malaya PHP<br>Issue date: 2026-12-09 |

**Steps**

1. Create proposal with test data.
2. Complete required fields and submit.
3. Issue the policy on the test issue date.

**Expected result:** Issuance is blocked with a message such as 'Agent designation not yet effective for this product'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-013 – Accept MP policy issued on effective date

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.2 |
| System | B |
| Module | Effective Date |
| Type / Priority | Boundary / High |
| Preconditions | Agnes Flores (MP) synced to System B |
| Test data | Agent: Agnes Flores (MP)<br>Product: Malaya PHP<br>Issue date: 2026-12-10 |

**Steps**

1. Create proposal with test data.
2. Submit and issue on the test issue date.

**Expected result:** Policy is issued successfully with Agnes Flores as writing agent.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-014 – Reject EP policy issued before effective date

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.2 |
| System | B |
| Module | Effective Date |
| Type / Priority | Boundary / High |
| Preconditions | Eric Torch (EP) synced to System B |
| Test data | Agent: Eric Torch (EP)<br>Product: AdvantageLife Pro USD<br>Issue date: 2026-12-09 |

**Steps**

1. Create proposal with test data.
2. Submit and issue on the test issue date.

**Expected result:** Issuance is blocked with the not-yet-effective message.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-015 – Accept EP policy issued on effective date

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.2 |
| System | B |
| Module | Effective Date |
| Type / Priority | Boundary / High |
| Preconditions | Eric Torch (EP) synced to System B |
| Test data | Agent: Eric Torch (EP)<br>Product: AdvantageLife Pro USD<br>Issue date: 2026-12-10 |

**Steps**

1. Create proposal with test data.
2. Submit and issue on the test issue date.

**Expected result:** Policy is issued successfully with Eric Torch as writing agent.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-016 – Existing designation not affected by new effective date

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.3 |
| System | B |
| Module | Effective Date |
| Type / Priority | Regression / High |
| Preconditions | Jane Santos (JFA) synced to System B |
| Test data | Agent: Jane Santos (JFA)<br>Product: Malaya PHP<br>Issue date: 2026-12-09 |

**Steps**

1. Create proposal with test data.
2. Submit and issue on the test issue date.

**Expected result:** Policy is issued successfully; the 2026-12-10 date applies only to MP and EP.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-017 – MP agent can select all four Zion products

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.4 |
| System | B |
| Module | Product Access |
| Type / Priority | Positive / High |
| Preconditions | Agnes Flores (MP) synced to System B |
| Test data | Agent: Agnes Flores (MP) |

**Steps**

1. Create proposal.
2. Enter Agnes Flores's agent code.
3. Open the Product dropdown.

**Expected result:** Dropdown lists Malaya PHP, Pangarap PHP, AdvantageLife Pro PHP and AdvantageLife Pro USD.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-018 – EP agent cannot select a non-Zion product

| Field | Detail |
|---|---|
| Story / AC | US-02 / AC-02.4 |
| System | B |
| Module | Product Access |
| Type / Priority | Negative / Medium |
| Preconditions | Eric Torch (EP) synced; GoldenYears PHP exists but not set up for Zion |
| Test data | Agent: Eric Torch (EP)<br>Product: GoldenYears PHP |

**Steps**

1. Create proposal.
2. Enter Eric Torch's agent code.
3. Look for GoldenYears PHP in the Product dropdown.

**Expected result:** GoldenYears PHP is not listed; only the four Zion product lines are available.

**Actual result:** _Not yet executed_ · **Status:** Not Run

### US-03 · Hierarchy setup

#### TC-019 – Verify record 103 SFA → MP

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.1 |
| System | A |
| Module | Hierarchy |
| Type / Priority | Positive / High |
| Preconditions | Hierarchy setup deployed |
| Test data | Reference code 103 |

**Steps**

1. Go to Hierarchy Setup > Zion.
2. Open reference code 103.

**Expected result:** Level 1 = SFA, Level 2 = MP; list view displays 'SFA → MP'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-020 – Verify record 104 MP → EP

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.1 |
| System | A |
| Module | Hierarchy |
| Type / Priority | Positive / High |
| Preconditions | Hierarchy setup deployed |
| Test data | Reference code 104 |

**Steps**

1. Go to Hierarchy Setup > Zion.
2. Open reference code 104.

**Expected result:** Level 1 = MP, Level 2 = EP; list view displays 'MP → EP'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-021 – Verify record 105 EP self-reporting

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.2 |
| System | A |
| Module | Hierarchy |
| Type / Priority | Positive / High |
| Preconditions | Hierarchy setup deployed |
| Test data | Reference code 105 |

**Steps**

1. Go to Hierarchy Setup > Zion.
2. Open reference code 105.

**Expected result:** Level 1 = EP, Level 2 = blank; EP is shown as self-reporting (top of hierarchy).

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-022 – Existing records 101 and 102 unchanged

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.3 |
| System | A |
| Module | Hierarchy |
| Type / Priority | Regression / High |
| Preconditions | Baseline of 101 and 102 captured |
| Test data | Reference codes 101, 102 |

**Steps**

1. Open reference codes 101 and 102.
2. Compare with baseline.

**Expected result:** 101: JFA = 1, FA = 2 (JFA → FA). 102: FA = 1, SFA = 2 (FA → SFA). No changes.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-023 – Full Zion chain is continuous with no gaps

| Field | Detail |
|---|---|
| Story / AC | US-03 / AC-03.1 |
| System | A |
| Module | Hierarchy |
| Type / Priority | Positive / Medium |
| Preconditions | Records 101–105 exist |
| Test data | All Zion hierarchy records |

**Steps**

1. Open Hierarchy Setup > Zion list view.
2. Trace from JFA upward.

**Expected result:** Chain reads JFA → FA → SFA → MP → EP with each designation appearing once as Level 1, and EP ending the chain.

**Actual result:** _Not yet executed_ · **Status:** Not Run

### US-04 · Agent profiles

#### TC-024 – Create EP agent with Self-reporting ticked

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.4 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Positive / High |
| Preconditions | Designations and hierarchy deployed |
| Test data | AG-01 Eric Torch, EP, Zion, licence Active (exp. 2028-12-31), Self-reporting? = ticked |

**Steps**

1. Go to Agents > Create Profile.
2. Enter test data, tick 'Self-reporting?'.
3. Click Save.

**Expected result:** Profile saves; upline field is blank/disabled; agent code is generated. Record the code in Test Data.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-025 – Reject EP agent without Self-reporting and no upline

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.4 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Negative / High |
| Preconditions | Agent creation screen open |
| Test data | Test EP agent, Self-reporting? = unticked, upline blank |

**Steps**

1. Enter test data.
2. Click Save.

**Expected result:** Save is blocked with a message such as 'Upline is required unless agent is self-reporting'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-026 – Self-reporting not allowed for non-EP designation

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.4 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Negative / High |
| Preconditions | Agent creation screen open |
| Test data | Test SFA agent, Self-reporting? = ticked |

**Steps**

1. Select designation SFA.
2. Try to tick 'Self-reporting?' and save.

**Expected result:** The tickbox is disabled for SFA, or save is blocked with 'Only EP can be self-reporting'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-027 – Create MP agent reporting to EP

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.2 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Positive / High |
| Preconditions | AG-01 Eric Torch exists |
| Test data | AG-02 Agnes Flores, MP, upline Eric Torch, licence Active |

**Steps**

1. Create profile with test data.
2. Click Save.

**Expected result:** Profile saves under Zion with upline Eric Torch; agent code generated.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-028 – Create SFA agent reporting to MP

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.2 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Positive / High |
| Preconditions | AG-02 Agnes Flores exists |
| Test data | AG-04 Neo Blake, SFA, upline Agnes Flores, licence Active |

**Steps**

1. Create profile with test data.
2. Click Save.

**Expected result:** Profile saves with upline Agnes Flores; agent code generated.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-029 – Create FA agent reporting to SFA

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.2 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Positive / High |
| Preconditions | AG-04 Neo Blake exists |
| Test data | AG-05 Charlie Hunt, FA, upline Neo Blake, licence Active |

**Steps**

1. Create profile with test data.
2. Click Save.

**Expected result:** Profile saves with upline Neo Blake; agent code generated.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-030 – Create JFA agent reporting to FA

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.2 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Positive / High |
| Preconditions | AG-05 Charlie Hunt exists |
| Test data | AG-07 Jane Santos, JFA, upline Charlie Hunt, licence Active |

**Steps**

1. Create profile with test data.
2. Click Save.

**Expected result:** Profile saves with upline Charlie Hunt; agent code generated. Agent tree shows Jane → Charlie → Neo → Agnes → Eric.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-031 – Agent codes are generated, unique and read-only

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.1 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Positive / High |
| Preconditions | AG-01 to AG-07 created |
| Test data | All 7 test agents |

**Steps**

1. Open each test agent profile.
2. Compare codes.
3. Try to edit the agent code field.

**Expected result:** Every agent has a code; no two codes are the same; the code field cannot be edited.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-032 – Reject JFA reporting directly to MP (skip)

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.3 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Negative / High |
| Preconditions | AG-02 Agnes Flores exists |
| Test data | Test JFA agent, upline Agnes Flores (MP) |

**Steps**

1. Create profile with test data.
2. Click Save.

**Expected result:** Save is blocked with a message such as 'Upline must hold the next higher designation (FA)'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-033 – Reject FA reporting directly to EP (skip)

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.3 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Negative / High |
| Preconditions | AG-01 Eric Torch exists |
| Test data | Test FA agent, upline Eric Torch (EP) |

**Steps**

1. Create profile with test data.
2. Click Save.

**Expected result:** Save is blocked; upline must be an SFA.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-034 – Reject SFA reporting directly to EP (skip)

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.3 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Negative / High |
| Preconditions | AG-01 Eric Torch exists |
| Test data | Test SFA agent, upline Eric Torch (EP) |

**Steps**

1. Create profile with test data.
2. Click Save.

**Expected result:** Save is blocked; upline must be an MP.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-035 – Reject MP reporting to a lower designation

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.3 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Negative / Medium |
| Preconditions | AG-04 Neo Blake exists |
| Test data | Test MP agent, upline Neo Blake (SFA) |

**Steps**

1. Create profile with test data.
2. Click Save.

**Expected result:** Save is blocked; upline must be an EP.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-036 – Save MP agent with expired licence

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.5 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Positive / High |
| Preconditions | AG-01 Eric Torch exists |
| Test data | AG-03 Paolo Reyes, MP, upline Eric Torch, licence expiry 2026-06-30 |

**Steps**

1. Create profile with test data.
2. Click Save.

**Expected result:** Profile saves; agent code generated; licence status shows 'Expired'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-037 – Save FA agent with expired licence

| Field | Detail |
|---|---|
| Story / AC | US-04 / AC-04.5 |
| System | A |
| Module | Agent Profile |
| Type / Priority | Positive / High |
| Preconditions | AG-04 Neo Blake exists |
| Test data | AG-06 Liza Cruz, FA, upline Neo Blake, licence expiry 2026-06-30 |

**Steps**

1. Create profile with test data.
2. Click Save.

**Expected result:** Profile saves; agent code generated; licence status shows 'Expired'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

### US-05 · System B sync & proposals

#### TC-038 – All test agents reach System B via API

| Field | Detail |
|---|---|
| Story / AC | US-05 / AC-05.1 |
| System | A → B |
| Module | API Sync |
| Type / Priority | Positive / High |
| Preconditions | AG-01 to AG-07 saved in System A; API job has run |
| Test data | All 7 test agents |

**Steps**

1. Check the API log for each agent.
2. Search each agent code in System B.

**Expected result:** Each agent exists in System B with the same code, name, designation, channel (Zion) and licence status as System A; API log shows success.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-039 – Agent code shows MP agent name

| Field | Detail |
|---|---|
| Story / AC | US-05 / AC-05.1 |
| System | B |
| Module | Proposal |
| Type / Priority | Positive / High |
| Preconditions | Agnes Flores synced |
| Test data | Agent code of Agnes Flores |

**Steps**

1. Create proposal.
2. Enter Agnes Flores's agent code.
3. Tab out of the field.

**Expected result:** Name 'Agnes Flores' is displayed for the code.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-040 – Agent code shows EP agent name

| Field | Detail |
|---|---|
| Story / AC | US-05 / AC-05.1 |
| System | B |
| Module | Proposal |
| Type / Priority | Positive / High |
| Preconditions | Eric Torch synced |
| Test data | Agent code of Eric Torch |

**Steps**

1. Create proposal.
2. Enter Eric Torch's agent code.
3. Tab out of the field.

**Expected result:** Name 'Eric Torch' is displayed for the code.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-041 – Unknown agent code shows an error

| Field | Detail |
|---|---|
| Story / AC | US-05 / AC-05.1 |
| System | B |
| Module | Proposal |
| Type / Priority | Negative / Medium |
| Preconditions | — |
| Test data | Agent code: 9999999 (does not exist) |

**Steps**

1. Create proposal.
2. Enter the test code.
3. Tab out of the field.

**Expected result:** No name is displayed; message such as 'Agent code not found'; proposal cannot be submitted.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-042 – Submit proposal with MP agent

| Field | Detail |
|---|---|
| Story / AC | US-05 / AC-05.2 |
| System | B |
| Module | Proposal |
| Type / Priority | Positive / High |
| Preconditions | Agnes Flores synced; issue date on/after 2026-12-10 |
| Test data | Agent: Agnes Flores (MP)<br>Product: Pangarap PHP<br>Issue date: 2026-12-10 |

**Steps**

1. Log in to System B as new business user.
2. Create a new proposal under Zion.
3. Enter agent code, product and test data.
4. Click Submit.

**Expected result:** Proposal is submitted successfully under Agnes Flores.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-043 – Submit proposal with EP agent

| Field | Detail |
|---|---|
| Story / AC | US-05 / AC-05.2 |
| System | B |
| Module | Proposal |
| Type / Priority | Positive / High |
| Preconditions | Eric Torch synced |
| Test data | Agent: Eric Torch (EP)<br>Product: AdvantageLife Pro PHP<br>Issue date: 2026-12-10 |

**Steps**

1. Log in to System B as new business user.
2. Create a new proposal under Zion.
3. Enter agent code, product and test data.
4. Click Submit.

**Expected result:** Proposal is submitted successfully under Eric Torch.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-044 – Submit proposal with existing-designation agent

| Field | Detail |
|---|---|
| Story / AC | US-05 / AC-05.2 |
| System | B |
| Module | Proposal |
| Type / Priority | Regression / Medium |
| Preconditions | Jane Santos synced |
| Test data | Agent: Jane Santos (JFA)<br>Product: AdvantageLife Pro USD<br>Issue date: 2026-12-10 |

**Steps**

1. Log in to System B as new business user.
2. Create a new proposal under Zion.
3. Enter agent code, product and test data.
4. Click Submit.

**Expected result:** Proposal is submitted successfully under Jane Santos.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-045 – Block proposal for MP agent with expired licence

| Field | Detail |
|---|---|
| Story / AC | US-05 / AC-05.3 |
| System | B |
| Module | Proposal |
| Type / Priority | Negative / High |
| Preconditions | Paolo Reyes synced with licence status Expired |
| Test data | Agent: Paolo Reyes (MP)<br>Product: Malaya PHP<br>Issue date: 2026-12-10 |

**Steps**

1. Log in to System B as new business user.
2. Create a new proposal under Zion.
3. Enter agent code, product and test data.
4. Click Submit.

**Expected result:** Submission is blocked with the message 'Agent License is expired'.

**Actual result:** _Not yet executed_ · **Status:** Not Run

#### TC-046 – Block proposal for FA agent with expired licence

| Field | Detail |
|---|---|
| Story / AC | US-05 / AC-05.3 |
| System | B |
| Module | Proposal |
| Type / Priority | Negative / High |
| Preconditions | Liza Cruz synced with licence status Expired |
| Test data | Agent: Liza Cruz (FA)<br>Product: Pangarap PHP<br>Issue date: 2026-12-10 |

**Steps**

1. Log in to System B as new business user.
2. Create a new proposal under Zion.
3. Enter agent code, product and test data.
4. Click Submit.

**Expected result:** Submission is blocked with the message 'Agent License is expired'.

**Actual result:** _Not yet executed_ · **Status:** Not Run
