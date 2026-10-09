# Backlog-Status

Stand: 2026-10-09 · Immer aktuell halten (siehe README, Schritte A–C).
Inhalt und Priorität der Stories: `user-stories.md` im Projekt-Repo. Hier steht nur **wo** jede Story steht.

## 1. Stories

| ID | Story | Priorität | Sprint | Status | Schätzung | Verantwortlich | ATs | Bemerkung |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| US-01 | Register an account | Must | 1 | Geplant | | | AT-01 | |
| US-02 | Sign in | Must | 1 | Geplant | | | AT-01 | |
| US-03 | Sign out | Must | 1 | Geplant | | | AT-01 | |
| US-04 | Manage planning preferences | Must | 1 | Geplant | | | AT-05 | |
| US-05 | Add a vehicle | Must | 1 | Geplant | | | AT-03, AT-04 | Detaillierte Story WF-01 (vorgeschlagen) |
| US-06 | View and select my vehicles | Must | 1 | Geplant | | | AT-04 | |
| US-07 | Delete a vehicle | Must (vorgeschlagen, OD-12) | 1 | Geplant | | | AT-19 | Priorität offen bis OD-12 entschieden |
| US-08 | Plan a direct route | Must | 2 | Backlog | | | AT-07, AT-08, AT-09, AT-16 | |
| US-09 | Override target and reserve | Must | 2 | Backlog | | | AT-06 | Kann nach S3 rutschen (Fallback) |
| US-10 | One charging stop (Epic) | Must | 2–3 | Backlog | – | – | via US-11/12 | Epic, keine eigene Zusage |
| US-11 | Charging route near reach limit | Must | 2 | Backlog | | | AT-10, AT-11 | Start kann nach S3 rutschen |
| US-12 | Bounded three-area search | Must | 3 | Backlog | | | AT-12 – AT-15 | Suchbereichserweiterung zuerst streichbar |
| US-13 | Understand why no route | Must | 2 (Teil) + 3 | Backlog | | | AT-06, AT-12, AT-15 | S2: direkte Route + Reserve; S3: Suche + Provider |
| US-14 | See the full route result | Must | 3 | Backlog | | | AT-16, AT-17 | |
| US-15 | Keyboard and small screens | Should | 3 | Backlog | | | AT-17 | Zuerst streichbar |
| TS-01 | Verify provider integration | Must | 2 | Backlog | | | AT-14, AT-16 | |
| TS-02 | Repeatable automated tests | Must | 1–3 | Backlog | | | AT-09, AT-13, AT-18 | Wächst mit jedem Sprint |

### Optionale Stories (nicht eingeplant)

| ID | Story | Priorität | Sprint | Status | Bemerkung |
| --- | --- | --- | --- | --- | --- |
| US-16 | Edit a vehicle | Should | – | Backlog | Erster Kandidat für freie Kapazität S3 |
| US-17 | Stations near a location | Should | – | Backlog | Nur nach Zustimmung PO |
| US-18 | Save a route | Could | – | Backlog | |
| US-19 | Address suggestions | Could | – | Backlog | |
| US-20 | Range plausibility warning | Could | – | Backlog | |
| US-21 | AC/DC, cable, adapter filter | Could | – | Backlog | |
| US-22 | Multiple charging stops | Could | – | Backlog | |
| US-23 | Duplicate / outdated responses | Should | – | Backlog | Erster Kandidat für freie Kapazität S3 |

## 2. Acceptance Tests

| AT | Geplant in Sprint | Stories | Status | Nachweis (CI-Lauf / Commit) | Datum |
| --- | --- | --- | --- | --- | --- |
| AT-01 | 1 | US-01, US-02, US-03 | Offen | | |
| AT-02 | 1 (querschnittlich) | Ownership-Constraint | Offen | | |
| AT-03 | 1 | US-05 | Offen | | |
| AT-04 | 1 | US-05, US-06 | Offen | | Fixtures; Live-OCM in S2 |
| AT-05 | 1 | US-04 | Offen | | |
| AT-06 | 2 | US-09, US-13 | Offen | | |
| AT-07 | 2 | US-08 | Offen | | |
| AT-08 | 2 | US-08 | Offen | | |
| AT-09 | 2 | US-08, TS-02 | Offen | | |
| AT-10 | 2 | US-11 | Offen | | |
| AT-11 | 2 | US-11 | Offen | | |
| AT-12 | 3 | US-12, US-13 | Offen | | |
| AT-13 | 3 | US-12, TS-02 | Offen | | |
| AT-14 | 3 | US-12, TS-01 | Offen | | |
| AT-15 | 3 | US-12, US-13 | Offen | | |
| AT-16 | 2 | US-08, US-14, TS-01 | Offen | | |
| AT-17 | 3 | US-14, US-15 | Offen | | OPT-08-Teil nur falls US-23 eingeplant |
| AT-18 | 3 | TS-02, Constraints | Offen | | |
| AT-19 | 1 | US-07 | Offen | | |

> AT-02 ist im Sprint-Plan nicht explizit Sprint 1 zugeordnet, gehört aber als Ownership-Constraint zu allen Sprint-1-Stories. Im nächsten Planning klären und ggf. im Changelog festhalten.

## 3. Offene Entscheidungen (OD) mit Sprintbezug

| OD | Thema | Benötigt bis | Status | Entscheidung / Datum |
| --- | --- | --- | --- | --- |
| OD-12 | Priorität US-07 | Review S1 | Offen | |
| OD-02 | Location match rule | Planning S2 | Offen | |
| OD-04 | OCM access / lifecycle mapping | Planning S2 | Offen | |
| OD-06 | Road distance → geometry | Planning S2 | Offen | |
| OD-05 | Partial provider failures | Planning S3 | Offen | |
| OD-07 | Shortlist | Planning S3 | Offen | |
| OD-09 | Usability-Kriterien US-15 | Planning S3 | Offen | |
| OD-10 | Qualitätsmetrik | Planning S3 | Offen | |
| – | Datum Zwischenpräsentation (Ereigniskarte) | so früh wie möglich | Offen | |
