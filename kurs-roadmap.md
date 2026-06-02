# Kurs-Roadmap: Tekniske roller

## Om roadmapet

Hvert roadmap består av 5–6 kursblokkert i naturlig progresjon. Blokkene er merket med koder:  
**[FELLES]** = går igjen i minst 4 av 6 retninger | **[DELT]** = delt mellom 2–3 retninger | *(ingen markering)* = unik kompetanse for rollen

---

## Fullstack Developer (FD)

| # | Kurstittel | Beskrivelse | Type |
|---|-----------|-------------|------|
| 1 | Programmeringsgrunnlag & versjonskontroll | Grunnleggende programmering, Git-flyt, branching-strategier og samarbeid i kodebasen | [FELLES] |
| 2 | Webutvikling: HTML/CSS/JS + rammeverk | Moderne frontend med React/Vue, responsivt design, komponentarkitektur | [DELT] |
| 3 | Backend & API-design | REST/GraphQL, serverside-logikk, databaser (SQL + NoSQL), ORM | [DELT] |
| 4 | Skyplattformer & deployment | Cloud-tjenester (AWS/Azure/GCP), containere, CI/CD-pipelines | [FELLES] |
| 5 | Testing & kodekvalitet | Enhetstesting, integrasjonstesting, TDD, linting og kodegjennomgang | [FELLES] |
| 6 | Systemdesign & arkitektur | Skalerbare systemer, mikrotjenester, caching, ytelseoptimalisering | [DELT] |

---

## Security Engineer (SEC)

| # | Kurstittel | Beskrivelse | Type |
|---|-----------|-------------|------|
| 1 | Programmeringsgrunnlag & versjonskontroll | Grunnleggende programmering, Git-flyt og samarbeid i kodebasen | [FELLES] |
| 2 | Nettverk & operativsystemer | TCP/IP, DNS, protokoller, Linux-administrasjon og nettverksarkitektur | Unik |
| 3 | Sikkerhetsprinsipper & trusselmodellering | CIA-triaden, OWASP, trusselanalyse, penetrasjonstesting og sårbarhetsskanning | Unik |
| 4 | Skyplattformer & deployment | IAM, nettverkssikkerhet i sky, compliance og sikker infrastruktur | [FELLES] |
| 5 | Testing & kodekvalitet | SAST/DAST, sikkerhetstesting, kodegjennomgang med sikkerhetsfokus | [FELLES] |
| 6 | Hendelseshåndtering & forensics | Incident response, logganalyse, SIEM, forensics og rapportering | Unik |

---

## DevOps Engineer (DO)

| # | Kurstittel | Beskrivelse | Type |
|---|-----------|-------------|------|
| 1 | Programmeringsgrunnlag & versjonskontroll | Scripting, Git-flyt, automatisering og infrastruktur som kode (IaC) | [FELLES] |
| 2 | Linux & serveradministrasjon | Shell-scripting, prosessadministrasjon, filsystemer og nettverkskonfigurasjon | Unik |
| 3 | Containere & orkestrering | Docker, Kubernetes, pod-administrasjon, service mesh og logging | Unik |
| 4 | Skyplattformer & deployment | Cloud-tjenester, Terraform, CI/CD-pipelines og release-strategier | [FELLES] |
| 5 | Testing & kodekvalitet | Automatisert testing av pipelines, infrastrukturtesting og overvåking | [FELLES] |
| 6 | Overvåking & observabilitet | Prometheus, Grafana, distributed tracing, alerting og SLO/SLA | [DELT] |

---

## Team Lead (TL)

| # | Kurstittel | Beskrivelse | Type |
|---|-----------|-------------|------|
| 1 | Programmeringsgrunnlag & versjonskontroll | Teknisk grunnlag, Git-flyt og forståelse av utviklingsprosessen | [FELLES] |
| 2 | Agile & prosjektledelse | Scrum, Kanban, sprintplanlegging, retroer og leveranseplanlegging | Unik |
| 3 | Systemdesign & arkitektur | Arkitekturbeslutninger, teknisk gjeld, ADR og fasilitering av designdiskusjoner | [DELT] |
| 4 | Skyplattformer & deployment | Forståelse av sky og pipelines for å støtte teamets leveranser | [FELLES] |
| 5 | Testing & kodekvalitet | Kodegjennomgangskultur, kvalitetsstandarder, definisjon av "done" | [FELLES] |
| 6 | Teamdynamikk & teknisk ledelse | Coaching, 1-1s, rekruttering, konflikthåndtering og psykologisk trygghet | Unik |

---

## Game Developer (GD)

| # | Kurstittel | Beskrivelse | Type |
|---|-----------|-------------|------|
| 1 | Programmeringsgrunnlag & versjonskontroll | C++/C#-grunnlag, Git-flyt og strukturert koding | [FELLES] |
| 2 | Spillmotorer & prototyping | Unity/Unreal Engine, scener, objekter, input-systemer og rask prototyping | Unik |
| 3 | 2D/3D-grafikk & animasjon | Shader-programmering, partikkelsystemer, animasjonsrigging og rendering | Unik |
| 4 | Spilldesign & mekanikk | Game loops, balansering, UX for spill, nivådesign og spillerfeedback | Unik |
| 5 | Testing & kodekvalitet | Playtesting, ytelseoptimalisering, bugsporingssystemer og QA-prosesser | [FELLES] |
| 6 | Skyplattformer & deployment | Distribusjon via Steam/konsoll/mobil, CI/CD for spill og multiplayer-infrastruktur | [FELLES] |

---

## Data Scientist (DS)

| # | Kurstittel | Beskrivelse | Type |
|---|-----------|-------------|------|
| 1 | Programmeringsgrunnlag & versjonskontroll | Python-grunnlag, Git-flyt, notebooks og reproduserbar kode | [FELLES] |
| 2 | Databehandling & statistikk | Pandas, NumPy, statistisk analyse, datarensing og eksplorativ analyse (EDA) | Unik |
| 3 | Maskinlæring & modellering | Supervised/unsupervised learning, scikit-learn, modellevaluering og feature engineering | Unik |
| 4 | Skyplattformer & deployment | MLOps, modell-serving, skalerbar databehandling og pipeline-orkestrering | [FELLES] |
| 5 | Testing & kodekvalitet | Datatesting, modellvalidering, reproduserbarhet og dokumentasjon | [FELLES] |
| 6 | Visualisering & kommunikasjon | Dashboards, storytelling med data, Tableau/Power BI og presentasjon for ikke-teknisk publikum | Unik |

---

## Overlappende blokker (oppsummering)

| Kurstittel | FD | SEC | DO | TL | GD | DS |
|-----------|:--:|:---:|:--:|:--:|:--:|:--:|
| Programmeringsgrunnlag & versjonskontroll | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Skyplattformer & deployment | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Testing & kodekvalitet | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Systemdesign & arkitektur | ✓ | – | – | ✓ | – | – |
| Backend & API-design | ✓ | – | – | – | – | – |
| Overvåking & observabilitet | – | – | ✓ | – | – | – |

---

## Blokkdiagram (ASCII-oversikt)

```
PROGRESJON →

FD:   [Prog.grunnlag] → [Webutvikling]      → [Backend & API]     → [Sky & Deploy] → [Testing & Kvalitet] → [Systemdesign]
SEC:  [Prog.grunnlag] → [Nettverk & OS]     → [Sikkerhetsprinsipper] → [Sky & Deploy] → [Testing & Kvalitet] → [Hendelseshåndtering]
DO:   [Prog.grunnlag] → [Linux & Server]    → [Containere & Ork.] → [Sky & Deploy] → [Testing & Kvalitet] → [Overvåking]
TL:   [Prog.grunnlag] → [Agile & Prosjekt]  → [Systemdesign]      → [Sky & Deploy] → [Testing & Kvalitet] → [Teamdynamikk]
GD:   [Prog.grunnlag] → [Spillmotorer]      → [Grafikk & Anim.]   → [Spilldesign]  → [Testing & Kvalitet] → [Sky & Deploy]
DS:   [Prog.grunnlag] → [Databehandling]    → [ML & Modellering]  → [Sky & Deploy] → [Testing & Kvalitet] → [Visualisering]

         ↑ FELLES ↑                                                      ↑ FELLES ↑        ↑ FELLES ↑
```
