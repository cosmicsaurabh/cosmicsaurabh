<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=240&color=0:020617,35:0F172A,70:0F766E,100:14B8A6&text=Saurabh%20Yadav&fontAlign=50&fontAlignY=38&desc=Mobile%20systems%20that%20stay%20correct%20under%20failure&descAlign=50&descAlignY=58&fontColor=FFFFFF&descColor=CCFBF1&fontSize=44&animation=fadeIn" alt="Saurabh — Mobile systems that stay correct under failure" />
</div>

<div align="center">
  <a href="mailto:saurabh.iiitk.job@gmail.com"><img src="https://img.shields.io/badge/Email-saurabh.iiitk.job%40gmail.com-111827?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://www.linkedin.com/in/cosmic-saurabh-yadav/"><img src="https://img.shields.io/badge/LinkedIn-Saurabh%20Yadav-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://github.com/cosmicsaurabh"><img src="https://img.shields.io/badge/GitHub-cosmicsaurabh-020617?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
  <a href="https://leetcode.com/u/cosmic_saurabh/"><img src="https://img.shields.io/badge/LeetCode-cosmic__saurabh-F59E0B?style=for-the-badge&logo=leetcode&logoColor=white" alt="LeetCode" /></a>
</div>

<div align="center">
  <img src="https://img.shields.io/badge/Focus-Mobile%20Engineering-14B8A6?style=flat-square" alt="Mobile Engineering" />
  <img src="https://img.shields.io/badge/Architecture-Offline--first-0F766E?style=flat-square" alt="Offline-first architecture" />
  <img src="https://img.shields.io/badge/Systems-Backend%20%2B%20Sync-0F172A?style=flat-square" alt="Backend and synchronization" />
  <img src="https://img.shields.io/badge/Priority-Reliability-334155?style=flat-square" alt="Reliability" />
</div>

## About

I am a mobile software engineer working across the Flutter/backend boundary: local persistence, synchronization, real-time state, media pipelines, API contracts, background work, and production failure recovery.

At [Reshape](https://reshapeapp.ai), I work primarily with Flutter/Dart and Node.js/TypeScript across offline data, camera and media workflows, streaming UX, AI-assisted product flows, real-time features, and automated testing.

I care about software that remains correct when networks are weak, responses are lost, work is retried, processes restart, and users move between sessions.

## Engineering mindset

| Principle | What it means in practice |
| --- | --- |
| **Local durability first** | Persist important user work before depending on network availability. |
| **Retry safety** | Use stable operation identities and idempotent boundaries after ambiguous responses. |
| **Explicit state** | Model long-running work as observable, recoverable state transitions. |
| **Operational clarity** | Preserve typed failures, useful telemetry, and testable side-effect boundaries. |
| **Proportional architecture** | Prefer the simplest design that satisfies the current reliability requirements. |

## Selected work

### [RythmRun](https://github.com/cosmicsaurabh/RythmRun) — offline-first GPS workout system

`Flutter` · `Riverpod` · `SQLite` · `TypeScript` · `Express` · `PostgreSQL` · `Prisma` · `Cloudflare R2`

> An end-to-end mobile and backend system built around the failure cases hidden behind a normal workout-tracking interface.

- Commits completed workouts, accepted route points, and status history in one SQLite transaction before attempting synchronization.
- Uses stable client-generated identities and PostgreSQL uniqueness constraints so a lost HTTP response can be retried without duplicating a workout.
- Filters noisy GPS samples through a versioned acceptance policy before calculating distance and pace.
- Persists image upload, replacement, and deletion as recoverable operations instead of treating them as single HTTP requests.
- Drains user-scoped synchronization and media work during account transitions to prevent cross-session races.

The repository documents its architecture, failure semantics, tests, known boundaries, and accepted trade-offs. It deliberately uses a modular monolith instead of introducing distributed infrastructure the workload does not require.

<p>
  <a href="https://github.com/cosmicsaurabh/RythmRun"><img src="https://img.shields.io/badge/Source-Repository-020617?style=for-the-badge&logo=github&logoColor=white" alt="RythmRun source" /></a>
  <a href="https://play.google.com/store/apps/details?id=com.github.cosmicsaurabh.rythmrun"><img src="https://img.shields.io/badge/Google%20Play-Live-16A34A?style=for-the-badge&logo=googleplay&logoColor=white" alt="RythmRun on Google Play" /></a>
  <a href="https://github.com/cosmicsaurabh/RythmRun/tree/main/docs/_engineering/improvement-plan"><img src="https://img.shields.io/badge/Engineering-Improvement%20Program-0F766E?style=for-the-badge" alt="RythmRun engineering improvement program" /></a>
</p>

### [LineLeap](https://github.com/cosmicsaurabh/LineLeap) — local-first sketch-to-image workflow

`Flutter` · `Provider` · `GetIt` · `Hive` · `Stable Horde API` · `GitHub Actions`

> A drawing and AI-generation application designed around long-running asynchronous work rather than a single loading screen.

- Provides a touch/stylus canvas with brush controls, undo/redo, clear, and mirror operations.
- Models generation as a persistent queue with explicit queued, submitting, generating, completed, failed, and retry states.
- Stores gallery metadata and generated images locally so completed work remains available without a network connection.
- Tests drawing-history and queue transitions and runs formatting, analysis, tests, and an Android build in CI.

<p>
  <a href="https://github.com/cosmicsaurabh/LineLeap"><img src="https://img.shields.io/badge/Source-Repository-020617?style=for-the-badge&logo=github&logoColor=white" alt="LineLeap source" /></a>
  <a href="https://flutter-scribble.web.app/"><img src="https://img.shields.io/badge/Web-Live%20Demo-0F766E?style=for-the-badge&logo=firebase&logoColor=white" alt="LineLeap web demo" /></a>
</p>

## Working set

<div align="center">
  <img src="https://skillicons.dev/icons?i=flutter,dart,kotlin,nodejs,ts,postgres,mongodb,redis,firebase,gcp,azure,git,githubactions&perline=13" alt="Flutter, Dart, Kotlin, Node.js, TypeScript, PostgreSQL, MongoDB, Redis, Firebase, GCP, Azure, Git, and GitHub Actions" />
</div>

| Area | Technologies and concerns |
| --- | --- |
| **Mobile** | Flutter, Dart, Riverpod, Provider, SQLite, Android/iOS integrations |
| **Backend and data** | Node.js, TypeScript, Express, PostgreSQL, Prisma, MongoDB, Redis |
| **Systems** | Offline-first synchronization, REST, WebSockets, SSE, idempotency, background work, media pipelines |
| **Delivery** | Automated tests, GitHub Actions, telemetry, feature flags, GCP, Azure, Firebase |

## How I use AI

I use AI tools to accelerate implementation, investigation, and review. I still own the problem definition, architecture, trade-offs, validation, and production outcome.

## GitHub activity

<div align="center">
  <img width="90%" src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=cosmicsaurabh&theme=github_dark" alt="Saurabh's GitHub contribution summary" />
</div>

## Connect

If you are working on mobile systems where reliability matters as much as the interface, I would enjoy comparing notes.

<div align="center">
  <a href="mailto:saurabh.iiitk.job@gmail.com"><img src="https://img.shields.io/badge/Start%20a%20conversation-Email%20me-14B8A6?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Saurabh" /></a>
</div>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:14B8A6,35:0F766E,70:0F172A,100:020617&height=110&section=footer" alt="Footer" />
</div>
