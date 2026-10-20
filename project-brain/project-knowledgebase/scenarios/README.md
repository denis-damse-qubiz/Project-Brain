# Scenarios

Scenarios are observable acceptance checks. Name each scenario file to match its related specification filename. Built rules need scenario coverage or a documented reason for exemption.

```md
# <Area>

## SC-<AREA>-001

- Covers: `R-<AREA>-001`
- Use case: <use case>
- Status: [planned]
- Priority: <priority>
- Setup: <required starting state>
- Steps:
  1. <action>
- Expected results:
  - <observable result>
```

Link scenarios only to sourced rules. Keep missing information as an open question rather than inventing behavior.
