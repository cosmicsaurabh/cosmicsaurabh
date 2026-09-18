# Saurabh Yadav

**Mobile software engineer building reliable Flutter systems and the services behind them.**

I work across the mobile/backend boundary: local persistence, synchronization, real-time state, media pipelines, API contracts, background work, and production failure recovery.

I care about software that remains correct when networks are weak, responses are lost, work is retried, processes restart, and users move between sessions.

[LinkedIn](https://www.linkedin.com/in/cosmic-saurabh-yadav/) · [Email](mailto:saurabh.iiitk.job@gmail.com) · [LeetCode](https://leetcode.com/u/cosmic_saurabh/)

## Engineering focus

- Establish local durability before depending on network availability.
- Make retries idempotent, especially after ambiguous responses.
- Model long-running work with explicit, recoverable states.
- Keep failures observable and architectural boundaries testable.
- Prefer the simplest design that satisfies the current reliability requirements.

In production, I work primarily with Flutter/Dart and Node.js/TypeScript across offline data, camera and media workflows, streaming UX, background execution, real-time features, and automated testing.

## Selected work

### [RythmRun](https://github.com/cosmicsaurabh/RythmRun) — offline-first GPS workout system

`Flutter` · `Riverpod` · `SQLite` · `TypeScript` · `Express` · `PostgreSQL` · `Prisma` · `Cloudflare R2`

RythmRun is an end-to-end mobile and backend system built around the failure cases hidden behind a normal workout-tracking UI.

- Commits completed workouts, accepted route points, and status history in one SQLite transaction before attempting synchronization.
- Uses stable client-generated identities and PostgreSQL uniqueness constraints so a lost HTTP response can be retried without duplicating a workout.
- Filters noisy GPS samples through a versioned acceptance policy before calculating distance and pace.
- Persists image upload, replacement, and deletion as recoverable operations rather than treating them as single HTTP requests.
- Drains user-scoped synchronization and media work during account transitions to prevent cross-session races.

The repository documents the architecture, failure semantics, design trade-offs, tests, and known boundaries. It deliberately uses a modular monolith instead of introducing distributed infrastructure the workload does not require.

[Source](https://github.com/cosmicsaurabh/RythmRun) · [Google Play](https://play.google.com/store/apps/details?id=com.github.cosmicsaurabh.rythmrun) · [Engineering improvement program](https://github.com/cosmicsaurabh/RythmRun/tree/main/docs/_engineering/improvement-plan)

### [LineLeap](https://github.com/cosmicsaurabh/LineLeap) — local-first sketch-to-image workflow

`Flutter` · `Provider` · `GetIt` · `Hive` · `Stable Horde API` · `GitHub Actions`

- Provides a touch/stylus canvas with brush controls, undo/redo, clear, and mirror operations.
- Models AI generation as a persistent queue with explicit queued, submitting, generating, completed, failed, and retry states.
- Stores gallery metadata and generated images locally so completed work remains available without a network connection.
- Tests drawing-history and queue transitions and runs formatting, analysis, tests, and an Android debug build in CI.

[Source](https://github.com/cosmicsaurabh/LineLeap) · [Web demo](https://flutter-scribble.web.app/)

## Working set

**Mobile:** Flutter, Dart, Riverpod, Provider, SQLite, Android/iOS integrations  
**Backend:** Node.js, TypeScript, Express, PostgreSQL, Prisma, MongoDB, Redis  
**Systems:** offline-first synchronization, REST, WebSockets, SSE, idempotency, background work, media pipelines  
**Delivery:** automated tests, GitHub Actions, telemetry, feature flags, GCP, Azure, Firebase

## How I use AI

I use AI tools to accelerate implementation, investigation, and review. I still own the problem definition, architecture, trade-offs, validation, and production outcome.

---

If you are working on mobile systems where reliability matters as much as the interface, I would enjoy comparing notes.

