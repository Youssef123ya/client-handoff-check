# Client Handoff Check - proposal text

## 1. What does the Skill do?

Client Handoff Check compares an approved project brief with a NAS delivery folder and produces an evidence-linked checklist of found, missing, and uncertain deliverables.

## 2. Who is the target user and problem?

Freelance designers and small creative teams can overlook promised exports during handoff because requirements and delivery files are scattered across project storage.

## 3. What is the proposed solution?

A scoped, read-only check connects explicit requirements to actual file evidence. Optional report saving happens only after review and approval.

## 4. What is the core user flow?

Select the governing brief and delivery folder; extract requirements; inventory authorized files; review the checklist; optionally approve saving a report outside the delivery folder.

## 5. How is it different?

The workflow checks promises against the actual delivery inventory, rather than only summarizing documents. Unknown coverage and ambiguous matches stay visible instead of producing an unsupported all-clear.

## 6. Which NAS capabilities are used, and when?

File discovery and metadata establish scope and inventory. Document reading extracts requirements and evidence. Supported text saving preserves an approved checklist alongside the project.

## 7. What is the technical approach?

The parent delegates ug-filesystem to file-agent, ug-document to document-agent, and ug-knowledge to knowledge-agent. Only verified completed results feed dependent steps. Each requirement is classified using explicit naming and coverage rules. Inputs are the approved brief, folder, and recursion choice. Platform-supported models process authorized data; local processing is preferred when available. No direct external API or custom executable is included.

## 8. What has been built, and what remains?

The Markdown Skill, evidence rules, report format, disclosures, and validation plan are implemented. The official static checker reports zero errors and warnings. Installation, expert outputs, permissions, and save behavior remain unverified on NAS.

## 9. How will you validate it as a Finalist?

Core test one checks a complete five-file delivery. Core test two detects two missing exports, then checks again after adding them. The edge case denies access to a subfolder: affected items must remain uncertain. Verify source integrity, evidence paths, approval handling, and saved-report confirmation.

## 10. What are the limits, risks, and dependencies?

File presence does not establish design quality, valid file contents, freshness, or client approval. Incomplete scans, concurrent edits, and document extraction errors limit conclusions. Uliya expert capabilities and available model processing are platform dependencies.

## Disclosures

Development reference/checker: official UGREEN uliya-skill-kit 0.7.3-en (catalog 2.0.0), from ai.ugreen.com/pages/hackathon-starter-kit;
governed by the linked UGREEN agreements. No standalone open-source license is asserted and no kit source is redistributed. Runtime:
proprietary Uliya experts under platform terms. No third-party code libraries are bundled in the Skill. Codex assisted analysis, authoring and static
checks. ElevenLabs generated concept-preview narration; Filmora assembled and exported that preview. These services use their proprietary
terms and are not runtime dependencies. Local artifact-production tools: ReportLab (BSD, reportlab.com), Pillow (MIT-CMU, python-pillow.org),
and FFmpeg (this build GPL v3 or later, ffmpeg.org). These tools are not bundled.
