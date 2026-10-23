# SmartLMS parity repair and production completion

## Comparison result

The uploaded project was extracted and inspected without running its code or modifying the application. All sidebar destinations were compared: student 18 → 17, teacher 17 → 17, administrator 17 → 18. Student AI Tutor is missing; administrator Certificates is an addition. Other destinations exist, but several nested workflows are reduced or disconnected.

The accompanying Files report contains the page-by-page matrix, source references, confirmed defects, unresolved checks and acceptance criteria. It supersedes older parity claims where current implementations already exist.

## Ordered stages

0. **Baseline:** restore test execution, reconcile an authorized schema-only inventory with current migrations and uploaded SQL, establish isolated fixtures and approve business-policy decisions.
1. **Security containment:** remove temporary-password disclosure; verify and atomically consume invitations; enforce password-change restrictions, authoritative session revocation, resource ownership, bounded validation, safe uploads and canonical-origin checks.
2. **Central foundations:** complete typed repository/provider boundaries, atomic operations, durable jobs, shared errors/DTOs, pagination, cache invalidation and notification contracts. Incrementally replace legacy calls, not the framework.
3. **Shared controls and truthful administration:** repair maintenance toggle, lock/unlock persistence, false-success feedback, inaccurate counts and fabricated health readings; consolidate support, account and broadcast interfaces.
4. **Learning and assessments:** restore topic-aware authoring/player and material metadata; assignment drafts/revisions/deletion; authoritative quiz resume; teacher results/manual grading; grading/regrade filters and deep links; complete normalized gradebook/export scope.
5. **Communication and study:** threaded discussions and attachments, calendar/planner integration and recurrence, automatic study collection/history, shared account/help/support and verified notifications/push.
6. **Admin operations and certificates:** safe course oversight, persisted invite inventory/revocation, full academic reports, broadcast history, accurate analytics, scheduled maintenance and reconciled certificate lifecycle.
7. **Live classes and proctoring:** embedded meeting lifecycle and attendance duration; authorized live feeds, monitoring/configuration and acknowledged interventions, with reconnect and URL fallback.
8. **AI, knowledge and voice:** scoped student tutor and justified teacher assistance; extraction/indexing/citations, server-side provider access, retained conversations and permission-aware voice. Human review remains required for published assessments/grades.
9. **Recovery and release:** safe cleanup, backup/restore drills, durable schedules, observability, route metadata, accessibility, load/runtime checks, staged rollout and rollback.

## Validation gates

- Every changed business rule gets a focused concrete-value test. Protected operations get anonymous, cross-role and cross-owner negative tests through the server interface.
- Repository contracts prove pagination, totals, errors and atomic behavior across replaceable adapters; migrations must both replay cleanly and upgrade fixtures.
- Verify authenticated student, teacher and admin workflows with realistic nonempty data, reload/read-back, uploads/downloads, deep links and failure states.
- Exercise datasets above existing page/report caps, concurrent attempts, stale versions, null/zero scores, unequal maxima, timezones and reconnects.
- Do not mark an operation successful from a toast alone. Confirm its persisted outcome, provider acknowledgment or truthful disabled state.
- Release requires no unresolved critical/high security findings, target-runtime evidence, recovery/rollback proof and owner-approved operational targets.

## Required decisions and limitations

Public privileged signup currently permits three admins and three teachers; invite-only provisioning is proposed, not silently approved. Grade weighting, certificate authority/state mapping, retention, quotas, maintenance exceptions and recovery targets require owner decisions before affected rules change.

The public homepage opened successfully and the latest available preview log reports build OK. Existing tests could not start because testing dependencies are missing. Live schema/provider settings, authenticated flows and multi-instance behavior remain unverified. No production certification, app repair, SQL execution or publication is included in this planning task.

## Technical constraints

Preserve TanStack Start, React, existing custom cookie authentication and server-only data access. Keep the chain frontend → typed actions/query layer → authorized server handlers → services/domain → typed repositories → replaceable database/storage adapters. Provider details stay server-only; no frontend database access or arbitrary database operations.

Retain certificate presentation snapshots at issuance and the shared client PDF renderer for previews/downloads. Reuse existing network banner, view toggle, live-proctoring/reporting, exports and persistence rather than duplicating them.