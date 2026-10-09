# Sprint 1 – Planning

Datum: 2026-10-05 · Zeitraum: 2026-10-05 bis 2026-10-18
Teilnehmende: [eintragen]
Status: nachträglich dokumentiert am 2026-10-09 aus `sprint-plan.md`; Werte in [ ] ergänzen

## 1. Sprint Goal

> A user can register, sign in, keep planning preferences, and manage owned vehicles (WF-01).

## 2. Ausgangslage

- Übernommen aus Sprint 0: [z. B. fehlende Schätzungen]
- Maßnahmen aus der Retro Sprint 0: [ ]
- Benötigte OD: **OD-12** (Priorität US-07) – bis zum Review klären

## 3. Kapazität

| Person | Verfügbare Stunden | Abwesenheiten |
| --- | --- | --- |
| [Name] | | |
| **Summe** | | |

Verbleibendes Budget vor Sprint 1: [ ] h von ca. 44 h · Geplant für Sprint 1: [ ] h

## 4. Sprint Backlog

| ID | Story | Priorität | Schätzung | Verantwortlich | ATs | Bemerkung |
| --- | --- | --- | --- | --- | --- | --- |
| US-01 | Register an account | Must | | | AT-01 | |
| US-02 | Sign in | Must | | | AT-01 | |
| US-03 | Sign out | Must | | | AT-01 | Kein Logout-Endpoint |
| US-04 | Manage planning preferences | Must | | | AT-05 | |
| US-05 | Add a vehicle | Must | | | AT-03, AT-04 | Detaillierte Story WF-01 |
| US-06 | View and select my vehicles | Must | | | AT-04 | |
| US-07 | Delete a vehicle | Must (vorgeschlagen, OD-12) | | | AT-19 | Erster Streichkandidat bei Zeitmangel |
| – | Ownership-Constraint | Must | – | | AT-02 | Querschnittlich, gilt für alle Stories |
| **Summe** | | | | | | |

## 5. Weitere Deliverables

- [ ] Backend- und Frontend-Grundgerüst
- [ ] CI mit Coverage-Tooling
- [ ] ADR-01 Layered architecture with provider adapters
- [ ] ADR-02 Controller responsibility
- [ ] ADR-03 Information Expert for range derivation
- [ ] Domänenmodell, Klassendiagramm, Datenmodell (User, Preferences, Vehicles)
- [ ] Detaillierte WF-01-Story mit Aktivitäts- und Sequenzdiagramm
- [ ] Wireframes: Sign-in, Settings, Vehicles
- [ ] Validierung und Fehleranzeige für diese Views
- [ ] AT-01 bis AT-05, AT-19 (AT-04 mit normalisierten Station-Fixtures; Live-OCM in Sprint 2)
- [ ] AI-Log aktuell

## 6. Risiken und Fallback

- Zeitmangel → US-07 streichen/verschieben (Entscheidung PO, OD-12)
- Schätzungen aus Sprint 0 fehlen → Kapazitätsvergleich mit 44 h nicht möglich

## 7. Abweichungen vom Sprint-Plan

- [Keine / ...]
