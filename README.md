# Scrum-Dokumentation – Anleitung

Stand: 2026-10-09 · Verantwortlich: Scrum Master

Dieses Repository ist die **Historie** des Projekts. Die fachlichen Dokumente bleiben im **Projekt-Repository**:

| Dokument | Ort | Rolle | Wer ändert es |
| --- | --- | --- | --- |
| `project-requirements.md` | Projekt-Repo, `docs/requirements/` | Quelle der Wahrheit für Regeln, FR/NFR/IC, AT, OD | Team mit Product Owner |
| `user-stories.md` | Projekt-Repo, `docs/requirements/` | Aktueller Stand der Stories (Inhalt, Priorität) | Team mit Product Owner |
| `sprint-plan.md` | Projekt-Repo, `docs/project/` | Aktueller Plan (Sprints, Ziele, Zuordnung) | Scrum Master nach Absprache |
| **dieses Repository** | eigenes GitHub-Repo | **Was wann geplant, erledigt, geändert wurde** | **Scrum Master** |

Projekt-Repository: [Link eintragen]

Wichtig: Ändert sich `user-stories.md` oder `sprint-plan.md` im Projekt-Repo, trägst du das hier in `changelog.md` ein – mit dem Commit-Hash aus dem Projekt-Repo. So bleiben beide Historien verbunden.

Regel: In diesem Repository wird **nichts gelöscht oder überschrieben**, was einmal abgeschlossen ist. Abgeschlossene Sprint-Ordner sind eingefroren. Korrekturen nur als neuer, datierter Eintrag.

## Ordnerstruktur

```
(Repository-Wurzel)
  README.md              ← diese Anleitung
  backlog-status.md      ← EINE Tabelle: Status jeder Story + jedes AT (immer aktuell)
  changelog.md           ← jede Änderung an Stories, Prioritäten, Plan, OD (nur anhängen)
  praesentation.md       ← Kennzahlen und Folieninhalte, wird nach jedem Review ergänzt
  _template/             ← Kopiervorlagen, nie direkt ausfüllen
    planning.md  log.md  review.md  retro.md
  sprint-0/  sprint-1/  sprint-2/ ...
    planning.md          ← eingefroren nach dem Planning
    log.md               ← laufend während des Sprints
    review.md            ← eingefroren nach dem Review
    retro.md             ← eingefroren nach der Retro
```

## Status-Werte (überall gleich verwenden)

| Status | Bedeutung |
| --- | --- |
| Backlog | Noch keinem Sprint zugeordnet |
| Geplant | Im Sprint Backlog, Arbeit noch nicht begonnen |
| In Arbeit | Jemand arbeitet daran |
| Fertig | Definition of Done erfüllt, AT noch nicht abgenommen |
| Abgenommen | Zugehörige AT grün, im Review vom PO akzeptiert |
| Verschoben → S*n* | In Sprint *n* verschoben (Grund im Changelog) |
| Gestrichen | Vom PO gestrichen (Grund im Changelog) |

AT-Status: **Offen** · **Grün** (mit CI-Lauf/Commit als Nachweis) · **Rot**.

---

## Ablauf – was du wann tust

### A) Sprint Planning (erster Tag des Sprints)

1. `_template/planning.md` nach `sprint-N/planning.md` kopieren und ausfüllen:
   Sprint Goal, Stories, Schätzung, verantwortliche Person, ATs, Kapazität.
   Die Stories kommen aus `sprint-plan.md` (Projekt-Repo) Abschnitt 2.
2. `_template/log.md` nach `sprint-N/log.md` kopieren.
3. In `backlog-status.md` die Stories des Sprints auf **Geplant** setzen und die Spalte *Sprint* eintragen.
4. Falls im Planning etwas vom Sprint-Plan abweicht: Eintrag in `changelog.md` **und** `sprint-plan.md` im Projekt-Repo anpassen.
5. Commit + Tag:
   ```
   git add . && git commit -m "Sprint N: Planning"
   git tag sprint-N-planning
   git push && git push --tags
   ```

### B) Während des Sprints (z. B. Montag und Donnerstag, 10 Minuten)

1. In `sprint-N/log.md` einen datierten Eintrag ergänzen (oben die Vorlage im Log).
2. In `backlog-status.md` Story-Status aktualisieren (Geplant → In Arbeit → Fertig).
3. Ändert sich eine Story, Priorität oder OD → `changelog.md` + betroffenes Dokument, dort das `Date`-Feld aktualisieren.
4. Commit und Push: `git add . && git commit -m "Sprint N: Status <Datum>" && git push` (kein Tag nötig).

### C) Sprint Review (letzter Tag)

1. `_template/review.md` nach `sprint-N/review.md` kopieren und ausfüllen.
2. In `backlog-status.md`: abgenommene Stories auf **Abgenommen**, ATs auf **Grün** mit Nachweis; Unfertiges auf **Verschoben → S*n+1***.
3. Verschiebungen in `changelog.md` eintragen und `sprint-plan.md` (Projekt-Repo) anpassen.
4. Kennzahlen des Sprints in `praesentation.md` Abschnitt 1 eintragen.

### D) Retrospektive (direkt danach)

1. `_template/retro.md` nach `sprint-N/retro.md` kopieren und ausfüllen (max. 3 Maßnahmen).
2. Maßnahmen der **vorherigen** Retro bewerten (umgesetzt? gewirkt?).
3. Commit + Tag:
   ```
   git add . && git commit -m "Sprint N: Review und Retro"
   git tag sprint-N-review
   git push && git push --tags
   ```

### E) Sonderfall Ereigniskarte (erwartet Ende Sprint 2)

1. Vor jeder Änderung: `git tag event-card-before` in **beiden** Repositories (= Backlog „vorher“).
2. In `changelog.md` einen Abschnitt „Ereigniskarte“ anlegen: Inhalt der Karte, betroffene Stories/FR/AT/Diagramme, Entscheidung des PO.
3. Stories, Sprint-Plan und `backlog-status.md` anpassen.
4. `git tag event-card-after` in beiden Repositories (= Backlog „nachher“).
5. Vergleich für die Präsentation:
   ```
   # hier: Status, Changelog, Sprint-Dateien
   git diff event-card-before event-card-after
   # im Projekt-Repo: Stories und Sprint-Plan
   git diff event-card-before event-card-after -- docs/requirements/user-stories.md docs/project/sprint-plan.md
   ```
   Tags pushen nicht vergessen: `git push --tags`

---

## Checkliste pro Sprint (zum Abhaken)

- [ ] `planning.md` ausgefüllt, Tag `sprint-N-planning`
- [ ] `log.md` mindestens 2× pro Woche ergänzt
- [ ] `backlog-status.md` aktuell
- [ ] Jede Änderung in `changelog.md`
- [ ] `review.md` mit AT-Nachweisen
- [ ] `retro.md` mit Maßnahmen
- [ ] `praesentation.md` Kennzahlen ergänzt
- [ ] Diagramme, ADRs und AI-Log aktualisiert (siehe Definition of Done)
- [ ] Tag `sprint-N-review`

## Sprintkalender

| Sprint | Zeitraum | Planning | Review + Retro |
| --- | --- | --- | --- |
| 0 | 2026-10-01 – 10-04 | 10-01 | 10-04 |
| 1 | 2026-10-05 – 10-18 | 10-05 | 10-18 (bzw. letzter Arbeitstag davor) |
| 2 | 2026-10-19 – 11-01 | 10-19 | 11-01 |
| 3 | 2026-11-02 – 11-15 | 11-02 | 11-15 |
| 4 | 2026-11-16 – 11-22 | 11-16 | 11-20 (interne Abgabe), Abgabe 11-22 |
