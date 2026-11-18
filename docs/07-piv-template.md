# Post-Implementation Verification (PIV) – Template

[← Back to README](../README.md)

Preventive action from [RCA DEF-001](06-rca.md). The person who performs a Production configuration change completes this document, usually as a Word file, and the BA/QA reviews it before go-live is announced.

## 1. Change details

| Field | Entry |
|---|---|
| Change / release reference | |
| Description | e.g. Add MP and EP designations to Zion channel |
| Environment | Production |
| System(s) | e.g. System A (DMS) |
| Setup performed by | |
| Setup date and time | |
| Approved setup list reference | e.g. Requirements doc / Test Data, section 2 |

## 2. Evidence rules

- One screenshot per configured item, or per screen if several items are clearly visible.
- **The desktop date and time must be visible in every screenshot** (include the taskbar clock).
- Screenshots must show the key values: code, description, product, effective dates.
- Check every item against the approved setup list, not from memory.

## 3. Verification checklist

Example filled in for the Zion MP and EP release:

| # | Item | Expected value | Screenshot ref | Matches? |
|---|---|---|---|---|
| 1 | Designation MP – Zion | Managing Partner | Fig. 1 | ☐ |
| 2 | Designation EP – Zion | Executive Partner | Fig. 2 | ☐ |
| 3 | MP – Malaya PHP | From 2026-12-10, To blank | Fig. 3 | ☐ |
| 4 | MP – Pangarap PHP | From 2026-12-10, To blank | Fig. 4 | ☐ |
| 5 | MP – AdvantageLife Pro PHP | From 2026-12-10, To blank | Fig. 5 | ☐ |
| 6 | MP – AdvantageLife Pro USD | From 2026-12-10, To blank | Fig. 6 | ☐ |
| 7 | EP – Malaya PHP | From 2026-12-10, To blank | Fig. 7 | ☐ |
| 8 | EP – Pangarap PHP | From 2026-12-10, To blank | Fig. 8 | ☐ |
| 9 | EP – AdvantageLife Pro PHP | From 2026-12-10, To blank | Fig. 9 | ☐ |
| 10 | EP – AdvantageLife Pro USD | From 2026-12-10, To blank | Fig. 10 | ☐ |
| 11 | Hierarchy 103 | SFA = 1, MP = 2 | Fig. 11 | ☐ |
| 12 | Hierarchy 104 | MP = 1, EP = 2 | Fig. 12 | ☐ |
| 13 | Hierarchy 105 | EP = 1, Level 2 blank | Fig. 13 | ☐ |

**Count check:** expected items 13 · verified items ___

## 4. Screenshots

Paste each screenshot under its figure number, with the desktop clock visible.

**Fig. 1 – Designation MP – Zion**
_[screenshot]_

…

## 5. Sign-off

| Role | Name | Date | Result |
|---|---|---|---|
| Prepared by (setup owner) | | | ☐ Complete |
| Reviewed by (BA/QA) | | | ☐ Verified ☐ Issues found |
| Approved for go-live | | | ☐ Approved |

If any item doesn't match, fix it, take a new screenshot and re-verify before sign-off.
