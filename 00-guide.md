# 00 Guide - How to fill SDLC docs

- Read this before filling any template in `~/.config/opencode/templates/flow/`.
- Each phase closes only when its Done below is met.
- Copy the template, never edit the template file itself.

## Index

- Phase 01 Requirements - Template `01-requirements.md` - Example `01-Requirements.md` - Done when scope plus REQ plus AC plus sign-off exist.
- Phase 02 Architecture - Template `02-architecture.md` - Example `02-Architecture.md` - Done when modules plus seams plus constraints plus 15-factor plus ADRs plus risks exist.
- Phase 03 Design - Template `03-design.md` - Example `03-Design.md` - Done when interface plus data plus behavior plus errors plus test hooks exist.
- Phase 04 Plan - Template `04-plan.md` - Example none yet - Done when split plus order plus estimate plus factor work exist.
- Phase 05 Code - Template `05-code.md` - Example none yet - Done when diff plus verification command plus regression test exist.
- Phase 06 Review QA - Template `06-review-qa.md` - Example none yet - Done when entry plus cases plus defects plus exit verdict exist.
- Phase 07 Staging - Template `07-staging.md` - Example none yet - Done when staging evidence plus go-no-go exist.
- Phase 08 Release - Template `08-release.md` - Example none yet - Done when notes plus rollout plus rollback verified exist.
- Phase 09 Support - Template `09-support.md` - Example none yet - Done when detect plus triage plus recover exist.

## 01 Requirements

- Write what the system shall do, not how.
- Each REQ needs one AC with Given when then.
- Out of scope must name code edits excluded in this step.
- Good: REQ-06 resume same thread across restart.
- Bad: system shall be fast with no metric because it cannot be tested.
- Template: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/SRS.md
- Example: https://www.reqview.com/doc/iso-iec-ieee-29148-srs-example/
- Example PDF: https://www.reqview.com/papers/ReqView-Example_Software_Requirements_Specification_SRS_Document.pdf
- Template LaTeX: https://github.com/wxinix/IEEE-29148-SRS-LaTeX-Template/blob/main/IEEE-29148-2018-SRS-Template.tex
- NFR: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/NFR.md

## 02 Architecture

- Name every module with one responsibility.
- Name every seam with owner on each side.
- List constraints code must not break.
- Fix 15-factor decisions here, not in code.
- Each ADR records winner plus why loser lost.
- A risk without mitigation blocks APPROVE.
- Template: https://github.com/foxcool/architecture-doc-template/blob/main/TEMPLATE.md
- Example: https://github.com/foxcool/architecture-doc-template/blob/main/examples/service-architecture.md
- Template ADR: https://github.com/bitsmuggler/arc42-c4-software-architecture-documentation-example/blob/main/adr-template.md

## 03 Design

- One module per file, link its architecture section.
- Define preconditions plus postconditions plus invariants per method.
- Cover empty plus null plus oversized plus concurrent plus auth plus downstream down.
- Every error case needs one test hook.
- A dependency without version plus fallback blocks APPROVE.
- Template HLD: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/HLD.md
- Template LLD: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/LLD.md
- Template API: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/api-spec-template.md
- Template data: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/data-architecture.md
- Template threat: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/threat-model.md
- Template ADR: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/ADR.md

## 04 Plan

- Split by files touched and Done per task.
- Order by dependency, blockers first.
- Include factor work inside tasks, not as extra.
- Bad: one big task called implement everything.
- Template Task: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/Task.md
- Template Story: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/Story.md
- Template EPIC: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/EPIC.md
- Template Feature: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/Feature.md
- Template RTM: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/RTM.md

## 05 Code

- Read implementation before using it.
- Grep callers before changing shared code.
- Show verification command with output.
- Bad: diff without test evidence.
- Template standards: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/coding-standards.md

## 06 Review QA

- Entry must be green before cases run.
- Each case traces to one REQ.
- Exit needs 100pct executed plus pass rate plus 0 open P0.
- Verdict is APPROVE or NEEDS-CHANGES or BLOCK.
- Template TestPlan: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/TestPlan.md

## 07 Staging

- Record what was tested, not just smoke passed.
- Rollback must be rehearsed in staging.
- Decision is GO or NO-GO with name plus date.

## 08 Release

- Notes come from merged work, not memory.
- Rollout names stages plus watch metric plus rollback threshold decided before rollout.
- Template notes: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/ReleaseNotes.md
- Template rollback: https://github.com/siddjoshi/AI-SDLC/blob/main/%20templates/RollbackPlan.md

## 09 Support

- Detect names alert plus dashboard.
- Triage names steps plus escalation condition.
- Recover links rollback plus postmortem.
