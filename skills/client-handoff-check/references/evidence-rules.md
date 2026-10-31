# Matching and evidence rules
These rules govern every checklist.

## Requirement ledger
For each requirement preserve its text, exact source identity, short excerpt, any real location returned by the expert, expected filename or subpath if explicit, quantity, and format. If a source location is unavailable say so; never invent a page or line. Conflicting briefs require user selection. Contradictions within the approved brief remain unresolved until the user clarifies them.

## Matching
1. Respect any explicit relative path. Otherwise look only within the authorized scope and recursion choice.
2. Compare literal filenames after documented platform path normalization. Preserve original spelling. Do not silently treat case variants as equivalent when filesystem semantics are unknown.
3. Multiple matching basenames in different directories require review unless an explicit subpath resolves the ambiguity.
4. Require a returned regular-file type and non-zero size for Found. Missing metadata, directories masquerading as files, and zero-byte files require review.
5. A filename extension establishes a named artifact, not that its bytes are valid for that format. File presence does not establish visual quality, correct dimensions, required internal content, freshness or client approval.
6. When a brief says "three social images" without identifying them, list candidates and ask the user to confirm which belong to the requirement. Do not automatically count unrelated images.
7. A draft file, alias or similar filename is not an exact match. Show it as a possible candidate for human review.
8. If a requirement is not assessable by file presence, mark Needs review with the reason. Do not silently remove it from the ledger.

## Coverage
Missing within checked scope is allowed only when enumeration is explicitly complete for every relevant authorized location and no uncertainty affects the requirement. A limit, depth cap, unreadable subfolder, unresolved link, permission error, unknown completeness or source extraction gap prevents an overall all-clear.
A verified empty directory is valid evidence of absence. An empty search response with unknown access or coverage is not.
Do not widen scope to resolve a miss without user authorization.

## Repeat runs
Read the source and inventory again. Do not reuse a previous report as current evidence. Keep saved reports outside the delivery directory. Concurrent changes can invalidate any non-atomic inventory; state that limitation and offer a fresh check rather than promising a frozen snapshot.

## Outcome language
Use Found, Missing within checked scope, or Needs review for each item.
Use "All N explicit filename requirements were found in the checked scope" only when every assessable named requirement has verified evidence and coverage is complete; follow it with the content-quality limitation.
Never say "safe to send", "client approved", "latest", or "fully compliant" based on this check.

