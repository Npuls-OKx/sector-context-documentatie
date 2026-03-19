# Agent-artifacten (traceerbare AI-sessies)

Hier slaan we **projectaanvragen**, **featureplannen** en **ontwerpdocumenten** op die (mede) met **Cursor-agents** zijn opgebouwd. Zo blijft zichtbaar **wat** wanneer is ontstaan en **welke mensen** verantwoordelijk waren (**human in the loop**).

## Mappen

| Map | Inhoud |
|-----|--------|
| [`project-requests/`](project-requests/) | Iteratieve projectaanvragen (`/project-aanvraag`) |
| [`feature-plans/`](feature-plans/) | Featureplannen uit een request (`/maak-plan`) |
| [`design-docs/`](design-docs/) | Ontwerp per feature (`/ontwerp-document`) |

## Bestandsnaam

Gebruik **UTC of lokale tijd + korte slug** (één bestand per “lijn” van werk, geen overschrijven zonder versienummer):

`YYYYMMDD_HHmm_<korte-beschrijving-kebab-case>.md`

Voorbeeld: `20260319_1430_okx-koppelvlak-projectaanvraag.md`

Bij **grote herziening** van hetzelfde onderwerp: nieuw bestand met nieuwe timestamp of suffix `_v2`.

## Verplichte kop (YAML frontmatter)

Elk bestand begint met:

```yaml
---
created: "2026-03-19T14:30:00+01:00"
updated: "2026-03-19T15:45:00+01:00"
human_authors:
  - "Naam (rol/organisatie)"
human_reviewers: []
agent_command: "project-aanvraag"
agent_model: ""
related_issues: []
source_paths: []
notes: "Asynchrone sessies: bij elke bewerking updated bijwerken en auteurs aanvullen indien meerdere mensen betrokken."
---
```

- **`human_authors`**: minstens één persoon die **inhoudelijk verantwoordelijk** is voor publicatie in de repo (niet de agent).
- **`updated`**: bij **elke** sessie/beurt die het bestand wijzigt.
- **`agent_command`**: welke slash-command de basis was (bijv. `project-aanvraag`, `maak-plan`, `ontwerp-document`).
- **`related_issues`**: optioneel GitHub-issue nummers als `["#12"]`.

Zie ook [`doc/Bijdragen-voor-beginners.md`](../../doc/Bijdragen-voor-beginners.md) (Cursor-workflow).
