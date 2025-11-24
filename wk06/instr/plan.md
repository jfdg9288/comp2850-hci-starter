# Week 6 – Instrumentation Plan (Week 9 Preview)

## Events to Log
- `task_created` – when a task is added
- `task_deleted` – when a task is deleted
- `validation_error` – when a form submission fails
- `filter_applied` (if added later) – when filters are used

Fields I might capture:
- `ts_iso` – timestamp in ISO format
- `session_id` – anonymous session identifier
- `request_id` – per-request ID
- `js_mode` – `js` vs `no-js`
- `task_id` – for edits/deletes
- `title_length` – length of task title
- `field` / `error_type` – for validation errors

## Metrics to Compute
- Time-on-task: how long to add/delete a task
- Error rate: how often validation errors occur per participant
- Completion rate: % of tasks completed successfully
- Filter usage rate: how often filters are used (if implemented)
- JS vs no-JS comparison: performance + errors

## Test Scenarios (for Week 9)
1. Add 3 tasks with realistic titles.
2. Delete one task using keyboard only.
3. (Later) Use filter/search, then reload the page and check persistence.

Notes:
- Metrics should help evaluate the backlog items marked `candidate_fix=true`.
- Instrumentation must avoid PII (no names, emails, IDs).
