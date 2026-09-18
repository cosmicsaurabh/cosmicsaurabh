<p align="center">
  <img src="./assets/profile-hero.svg" width="100%" alt="Saurabh — Mobile and AI product engineer with 2+ years of production experience" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Open%20to-Mobile%20%2F%20Flutter%20%2F%20AI%20Product%20Roles-4F46E5?style=for-the-badge" alt="Open to mobile, Flutter, and AI product engineering roles" />
  <a href="mailto:saurabh.iiitk.job@gmail.com"><img src="https://img.shields.io/badge/Email-1E293B?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://www.linkedin.com/in/cosmic-saurabh-yadav/"><img src="https://img.shields.io/badge/LinkedIn-2563EB?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Location-India%20·%20Bengaluru%20·%20Hyderabad%20·%20Remote-312E81?style=flat-square" alt="Open to roles in India, Bengaluru, Hyderabad, and remote" />
  <a href="https://leetcode.com/u/cosmic_saurabh/"><img src="https://img.shields.io/badge/DSA-1%2C000%2B%20problems-7C3AED?style=flat-square&logo=leetcode&logoColor=white" alt="More than 1,000 DSA problems solved" /></a>
</p>

<p align="center"><sub>PRODUCTION CONTEXT AT RESHAPE</sub></p>

<table>
  <tr>
    <td width="25%" align="center"><strong>100K+</strong><br/><sub>mobile installs</sub></td>
    <td width="25%" align="center"><strong>1.2M+</strong><br/><sub>meals logged</sub></td>
    <td width="25%" align="center"><strong>133K+</strong><br/><sub>AI coach messages</sub></td>
    <td width="25%" align="center"><strong>80+</strong><br/><sub>typed AI actions</sub></td>
  </tr>
</table>

## What I can own

I build product flows that cross the mobile/backend boundary. My work does not stop at a screen: I follow state through local persistence, APIs, asynchronous execution, AI providers, databases, telemetry, tests, and production failure recovery.

<table>
  <tr>
    <td width="50%" valign="top">
      <strong>End-to-end mobile delivery</strong><br/>
      Flutter architecture, state management, native integrations, local data, networking, performance, and release-ready UX.
    </td>
    <td width="50%" valign="top">
      <strong>Production AI workflows</strong><br/>
      Multimodal input, structured schemas, typed tool execution, streaming, cancellation, retries, and provider failure handling.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <strong>Reliability under failure</strong><br/>
      Offline-first persistence, idempotent operations, durable outboxes, lifecycle recovery, caching, and observable terminal states.
    </td>
    <td width="50%" valign="top">
      <strong>Backend and data boundaries</strong><br/>
      Node.js/TypeScript services, API contracts, PostgreSQL, MongoDB, Redis, background workers, cloud infrastructure, and tests.
    </td>
  </tr>
</table>

## Production engineering highlights

| System | What I delivered | Signal |
| --- | --- | --- |
| **Multimodal meal logging** | Owned mobile architecture across photo, text, and voice analysis; moved execution into client/backend workflows with streaming state, background work, retries, cancellation, and recovery. | **1.2M+ meals**; client-side failures reduced **10%** |
| **Fio AI coach** | Built the Flutter tool-execution layer that converts structured model output into contextual read/write actions across health domains. | **133K+ messages**, **11.8K users**, **80+ actions**; workflow errors down ~**30%**, latency down **50%** |
| **Workout product** | Redesigned tracking flows, state management, analytics visualizations, and supporting data behavior. | Workout-section retention improved **60%** |
| **Social and media** | Delivered cursor pagination, optimistic interactions, persistent outboxes, WebSocket activity, privacy controls, protected media, viewport-aware caching, and tests. | Production system supporting **26K+ posts** |
| **Personalized weekly report** | Built an interactive cross-domain report with cached Home states, PDF export, experiment rollout, persisted feedback, and widget tests. | Mobile + backend feature delivered across product, data, and feedback boundaries |

## How the pieces connect

```mermaid
flowchart LR
    UI["Flutter UI"] --> STATE["Explicit app state"]
    STATE --> LOCAL[("SQLite + files")]
    LOCAL --> QUEUE["Outbox / sync"]
    QUEUE --> API["Node.js / TypeScript API"]
    API --> DATA[("PostgreSQL")]
    API --> ORCH["AI orchestration"]
    ORCH --> MODELS["LLM + vision providers"]
    ORCH --> TOOLS["Typed read / write tools"]
    ORCH -. "streaming + typed errors" .-> STATE
    STATE <--> LIVE["WebSockets / SSE"]
    STATE --> MEDIA["Camera + media"]
    MEDIA --> OBJECTS[("Object storage")]

    classDef mobile fill:#172554,stroke:#60A5FA,color:#FFFFFF;
    classDef state fill:#312E81,stroke:#A5B4FC,color:#FFFFFF;
    classDef service fill:#4C1D95,stroke:#C4B5FD,color:#FFFFFF;
    classDef ai fill:#581C87,stroke:#E879F9,color:#FFFFFF;
    classDef data fill:#0F172A,stroke:#94A3B8,color:#FFFFFF;
    class UI mobile;
    class STATE,QUEUE state;
    class API,LIVE,MEDIA service;
    class ORCH,MODELS,TOOLS ai;
    class LOCAL,DATA,OBJECTS data;
```

## Open-source proof

### [RythmRun](https://github.com/cosmicsaurabh/RythmRun) — offline-first GPS workout system

`Flutter` · `Riverpod` · `SQLite` · `TypeScript` · `Express` · `PostgreSQL` · `Prisma` · `Cloudflare R2`

- Commits completed workouts, accepted route points, and status history in one SQLite transaction before synchronization.
- Uses stable client-generated identities and PostgreSQL uniqueness so ambiguous HTTP retries cannot duplicate a workout.
- Applies a versioned GPS acceptance policy before calculating distance and pace.
- Persists image upload, replacement, and deletion as recoverable state machines.
- Documents architecture, failure semantics, tests, known boundaries, and accepted trade-offs.

<p>
  <a href="https://github.com/cosmicsaurabh/RythmRun"><img src="https://img.shields.io/badge/Inspect-the%20source-020617?style=for-the-badge&logo=github&logoColor=white" alt="Inspect RythmRun source" /></a>
  <a href="https://play.google.com/store/apps/details?id=com.github.cosmicsaurabh.rythmrun"><img src="https://img.shields.io/badge/Run-the%20app-2563EB?style=for-the-badge&logo=googleplay&logoColor=white" alt="RythmRun on Google Play" /></a>
  <a href="https://github.com/cosmicsaurabh/RythmRun/tree/main/docs/_engineering/improvement-plan"><img src="https://img.shields.io/badge/Read-the%20trade--offs-7C3AED?style=for-the-badge" alt="RythmRun engineering improvement program" /></a>
</p>

### [LineLeap](https://github.com/cosmicsaurabh/LineLeap) — persistent AI generation workflow

`Flutter` · `Provider` · `GetIt` · `Hive` · `Stable Horde API` · `GitHub Actions`

- Models AI generation as a persistent queue with queued, submitting, generating, completed, failed, and retry states.
- Stores gallery metadata and generated images locally so completed work survives navigation and remains available offline.
- Tests drawing history and queue transitions and runs formatting, analysis, tests, and an Android build in CI.

<p>
  <a href="https://github.com/cosmicsaurabh/LineLeap"><img src="https://img.shields.io/badge/Inspect-the%20source-020617?style=for-the-badge&logo=github&logoColor=white" alt="Inspect LineLeap source" /></a>
  <a href="https://flutter-scribble.web.app/"><img src="https://img.shields.io/badge/Try-the%20web%20demo-4F46E5?style=for-the-badge&logo=firebase&logoColor=white" alt="LineLeap web demo" /></a>
</p>

## Technical range

<p align="center">
  <img src="https://skillicons.dev/icons?i=flutter,dart,kotlin,nodejs,ts,postgres,mongodb,redis,firebase,gcp,azure,git,githubactions&perline=13" alt="Flutter, Dart, Kotlin, Node.js, TypeScript, PostgreSQL, MongoDB, Redis, Firebase, GCP, Azure, Git, and GitHub Actions" />
</p>

| Area | Working set |
| --- | --- |
| **Mobile** | Flutter, Dart, Riverpod, Provider, SQLite, camera/media, background execution, Android/iOS integrations |
| **AI product engineering** | Multimodal input, model orchestration, structured schemas, function calling, typed tools, streaming, cancellation, failure recovery |
| **Backend and data** | Node.js, TypeScript, Express, PostgreSQL, Prisma, MongoDB, Redis, REST, WebSockets, SSE |
| **Quality and delivery** | Widget/integration tests, Jest, telemetry, feature flags, GitHub Actions, GCP, Azure, Firebase |

> AI accelerates my implementation, investigation, and review. I remain accountable for the problem definition, architecture, trade-offs, validation, and production outcome.

<details>
  <summary><strong>GitHub activity</strong></summary>
  <br/>
  <p align="center">
    <img width="92%" src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=cosmicsaurabh&theme=github_dark" alt="Saurabh's GitHub contribution summary" />
  </p>
</details>

---

<p align="center">
  <strong>Hiring for mobile, Flutter, or AI product engineering?</strong><br/>
  I am interested in teams solving real product and reliability problems—not just shipping screens.<br/><br/>
  <a href="mailto:saurabh.iiitk.job@gmail.com"><img src="https://img.shields.io/badge/Start%20a%20conversation-2563EB?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Saurabh" /></a>
</p>
