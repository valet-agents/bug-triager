---
name: triage
description: Triage a Sentry alert — classify severity, review code, and create or update a Linear ticket
---

# Triage

Triage a Sentry alert end-to-end.

## Steps

1. Parse the Sentry alert payload to extract the error type,
   message, stack trace, project, environment, and event count.
2. Fetch additional context from Sentry if the payload is
   incomplete (e.g. full stack trace, tags, breadcrumbs).
3. Classify severity:
   - **Critical** — production-breaking, data loss, security
   - **High** — significant user impact, frequent occurrence
   - **Medium** — noticeable but limited impact
   - **Low** — cosmetic, rare, or non-user-facing
4. Read the source files from GitHub that appear in the stack
   trace. Identify the likely root cause.
5. Search Linear for an existing ticket that matches this error
   (by title or error fingerprint). If found, update it with
   the latest occurrence data and any revised diagnosis.
   Otherwise create a new ticket.
6. The Linear ticket must include:
   - Title matching the error
   - Severity label
   - Diagnosis section explaining the likely cause
   - Summarized stack trace
   - Link to the Sentry issue
