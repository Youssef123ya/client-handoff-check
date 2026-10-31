# Client Handoff Check

A Uliya Skill that checks the files promised in an approved project brief against an authorized NAS delivery folder.

**Status:** Round 1 orchestration Skill authored and statically validated. Actual installation and NAS runtime testing remain pending.

- [Devpost entry](https://devpost.com/software/client-handoff-check)
- [YouTube concept preview](https://youtu.be/FsOqcpfg5T0)
- [Round 1 Skill ZIP](dist/client-handoff-check-v1.0.0.zip)
- [Proposal PDF](docs/client-handoff-check-proposal.pdf)
- [Editable proposal text](docs/proposal.md)

The video uses illustrative cards, not real NAS execution footage. It is not the required Round 2 final demo.

## What it does
The intended workflow reads one approved brief, inventories one authorized delivery scope, and returns an evidence-linked checklist:
- **Found**: a unique explicitly named file has verified presence, type and non-zero size.
- **Missing within checked scope**: the file is absent from a completely enumerated authorized scope.
- **Needs review**: ambiguous names, incomplete coverage, unreadable sources, zero-byte files or requirements that need human judgment.

The source check is read-only. Saving the reviewed checklist is optional, separately approved and outside the delivery directory.

## Repository structure
- `skills/client-handoff-check/SKILL.md`: runtime entry point.
- `skills/client-handoff-check/references/`: evidence rules, report format, validation plan and disclosures.
- `dist/`: the Markdown-only contest package.
- `docs/`: proposal and local validation record.
- `demo-fixtures/`: original synthetic inputs for future NAS validation.

The contest ZIP contains only SKILL.md and its directly linked Markdown references. Repository documentation, fixtures and release records are separate from that runtime package.

## How to use
1. Read the [official UGREEN starter-kit instructions](https://ai.ugreen.com/pages/hackathon-starter-kit).
2. Follow the actual installation/import process provided for the assigned UGREEN NAS environment.
3. Supply the identity of the approved brief, the authorized delivery directory and whether its subfolders are included.
4. Try: "Check my delivery folder against the approved brief and tell me which promised files are present, missing, or need review."
5. Review the evidence and coverage. Optionally approve saving the exact report to a separate destination.

No local server, Python runtime or custom executable is required by this Skill. The actual NAS work is performed by Uliya's registered experts.

## Architecture
- `ug-document` -> `document-agent`: read explicit requirements and evidence.
- `ug-filesystem` -> `file-agent`: discover files and verify metadata.
- Parent Skill: reason over verified results and preserve uncertainty.
- `ug-knowledge` -> `knowledge-agent`: save an approved report with verified completion.

The parent delegates supported work; it does not directly invoke CLIs or access NAS files.

## Validation
Official uliya-skill-kit 0.7.3-en, capability catalog 2.0.0:
- Static result: **static-pass**
- Errors: **0**
- Warnings: **0**

See [the exact checker output](docs/check-results.json) and [the NAS test plan](skills/client-handoff-check/references/validation.md).

The synthetic complete fixture contains all five explicitly named files. The incomplete fixture omits logo.png and social-03.png; a similarly named draft must not substitute for either. These fixtures are test inputs, not a record of executed NAS tests.

## Limits
File presence does not establish file-format integrity, creative quality, latest-version status, client approval or an atomic snapshot. Incomplete enumeration and ambiguous or broad requirements require human review.
Model availability, offline operation, expert output compatibility, permissions and save collision handling still need target-device validation.

## Tools and provenance
This Skill and its core workflow were newly authored for UGREEN Hackathon 2026, starting October 30, 2026. Codex assisted requirement analysis, authoring, static checks and artifact production. ElevenLabs generated concept-preview narration; Filmora assembled and exported the video.

The official creation kit was used as development guidance and a checker. Its implementation is not redistributed here. See [full sources and license disclosures](skills/client-handoff-check/references/disclosures.md). No additional open-source license has been selected for the original project files.

