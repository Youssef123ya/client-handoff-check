# Checklist report format
Return Markdown in English unless the user requests a different interaction language. Hackathon materials remain English.

## Header
- Approved brief: actual returned identity.
- Delivery scope: actual returned identity and authorized recursion.
- Coverage: Complete, Incomplete, or Unknown, with exact limits and inaccessible locations.
- Evidence freshness: this check uses the current expert results; concurrent edits are not locked.
- Scope: file presence and explicit naming only.

## Requirements table
Use columns: Requirement | Status | Brief evidence | File evidence | Next step.
One row per explicit requirement. Quote a short source excerpt and use only locations actually returned by the document expert. File evidence contains the real returned path, type and size where available. For missing items state the completely checked scope; do not invent a file path or identifier.

Keep unresolved requirements and source-reading gaps visible. Separate explicit filename requirements from broader requirements needing human review. Report counts for Found, Missing within checked scope, and Needs review, without hiding unassessed content.

## Follow-up
List the smallest practical actions: add a missing export, clarify an ambiguous candidate, or narrow an incomplete scan. Do not take those actions automatically.

## Save result
If the user declines saving: "Checklist displayed; no report save requested."
If approval is pending: state waiting_approval and the approved destination.
If saved: state the actual outputFile only after completed and verified=true.
If failed or uncertain: preserve the displayed report and state the exact save status. Never claim a successful save or repeat it blindly.

## Required limitation
"This checklist verifies file presence against the readable brief and checked directory scope. It does not verify creative quality, file-format integrity, client approval, or an atomic snapshot of changing files."

