# Changelog

Nur **anhängen**, nie ändern oder löschen. Neueste Einträge unten.
Jede Änderung an Stories, Prioritäten, Sprint-Zuordnung, Open Decisions oder am Sprint-Plan gehört hierher.

## Vorlage für einen Eintrag

```
### JJJJ-MM-TT – <kurzer Titel>
- **Art:** Story neu | Story geändert | Priorität | Sprint-Zuordnung | OD entschieden | Plan | Ereigniskarte
- **Betroffen:** US-.., AT-.., FR-.., Dokument(e)
- **Vorher:** ...
- **Nachher:** ...
- **Grund:** ...
- **Entschieden von:** PO / Team
- **Commit/Tag:** ...
```

---

## Einträge

### 2026-10-01 – Sprint-Plan-Entwurf und User-Stories-Entwurf erstellt
- **Art:** Plan
- **Betroffen:** `sprint-plan.md`, `user-stories.md`
- **Vorher:** Projektskizze mit 3 undatierten Sprints und Backlog PB-01 bis PB-12
- **Nachher:** Sprint 0–4 mit Daten; Stories US-01 bis US-23, TS-01, TS-02; Mapping PB → US in `user-stories.md` Abschnitt 10
- **Grund:** Konkretisierung für Sprint 1
- **Entschieden von:** Team (Entwurf, PO-Review ausstehend)
- **Commit/Tag:** [eintragen]

### 2026-10-01 – Stories zusammengelegt bzw. in Constraints überführt
- **Art:** Story geändert
- **Betroffen:** `user-stories.md` Abschnitt 11
- **Vorher:** Einzelne Stories „Keep my data private“, „Add a vehicle by capacity and consumption“, „State my current charge“, „Learn that no charging is needed“, „Keep provider keys and passwords safe“, „Limit provider requests and waiting time“, „Prepare UI text for translation“
- **Nachher:** Querschnitts-Constraints (Abschnitt 7), Szenario von US-05, Teil von US-08 bzw. US-12
- **Grund:** Keine eigenständigen Nutzerziele; Doppelungen vermeiden
- **Entschieden von:** Team
- **Commit/Tag:** [eintragen]

### 2026-10-01 – PB-10 von Could auf Must
- **Art:** Priorität
- **Betroffen:** PB-10 → US-05
- **Vorher:** Reichweite aus Kapazität und Verbrauch = Could
- **Nachher:** Must, als Alternativszenario von US-05
- **Grund:** Nutzer kennen ihre Reichweite oft nicht
- **Entschieden von:** [PO bestätigen]
- **Commit/Tag:** [eintragen]

### 2026-10-05 – User Stories neu nummeriert
- **Art:** Story geändert
- **Betroffen:** `user-stories.md`
- **Vorher:** [alte Nummerierung]
- **Nachher:** IDs in Dokumentreihenfolge, ab jetzt stabil; zurückgezogene IDs werden nicht wiederverwendet
- **Grund:** Konsistente Referenzen in Plan und Tests
- **Entschieden von:** Team
- **Commit/Tag:** [eintragen]
- **Hinweis:** `Date`-Feld in `user-stories.md` steht noch auf 2026-10-01 → aktualisieren
