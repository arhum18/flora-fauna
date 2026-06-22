# Flora & Fauna — Plant Encyclopedia

A Wikipedia-style plant encyclopedia database. Entries follow a structured JSON template validated against a shared schema, making the data easy to fill in, query, and extend.

---

## Repository Structure

```
flora-fauna/
├── schema/
│   └── plant-entry.schema.json        # JSON Schema defining all encyclopedia entry fields
└── encyclopedia/
    ├── cycads/                         # Division: Cycadophyta
    │   ├── README.md                   # Category overview
    │   ├── cycas.json
    │   ├── encephalartos.json
    │   ├── zamia.json
    │   ├── ceratozamia.json
    │   ├── lepidozamia.json
    │   ├── macrozamia.json
    │   ├── dioon.json
    │   ├── microcycas.json
    │   ├── stangeria.json
    │   └── bowenia.json
    ├── liverworts-and-hornworts/       # Divisions: Marchantiophyta & Anthocerotophyta
    │   └── template.json
    ├── flowering-plants/               # Division: Angiospermae
    │   └── template.json
    ├── mosses/                         # Division: Bryophyta
    │   └── template.json
    └── conifers/                       # Division: Pinophyta
        └── template.json
```

---

## Plant Categories

| Category | Division | Template status |
|---|---|---|
| [Cycads](encyclopedia/cycads/README.md) | Cycadophyta | ✅ 10 genus templates created |
| [Liverworts & Hornworts](encyclopedia/liverworts-and-hornworts/template.json) | Marchantiophyta / Anthocerotophyta | ✅ Category template created |
| [Flowering Plants](encyclopedia/flowering-plants/template.json) | Angiospermae | ✅ Category template created |
| [Mosses](encyclopedia/mosses/template.json) | Bryophyta | ✅ Category template created |
| [Conifers](encyclopedia/conifers/template.json) | Pinophyta | ✅ Category template created |

---

## Cycad Genera (detailed templates)

| Genus | Family | Notable feature |
|---|---|---|
| [*Cycas*](encyclopedia/cycads/cycas.json) | Cycadaceae | Oldest/most widespread cycad genus |
| [*Encephalartos*](encyclopedia/cycads/encephalartos.json) | Zamiaceae | African cycads; most threatened group |
| [*Zamia*](encyclopedia/cycads/zamia.json) | Zamiaceae | Largest New World genus |
| [*Ceratozamia*](encyclopedia/cycads/ceratozamia.json) | Zamiaceae | Horned cone scales; Mexican cloud forests |
| [*Lepidozamia*](encyclopedia/cycads/lepidozamia.json) | Zamiaceae | Among world's tallest cycads; Australian endemic |
| [*Macrozamia*](encyclopedia/cycads/macrozamia.json) | Zamiaceae | Australian endemic; fire-adapted |
| [*Dioon*](encyclopedia/cycads/dioon.json) | Zamiaceae | Heaviest cones; drought-tolerant; Mexico |
| [*Microcycas*](encyclopedia/cycads/microcycas.json) | Zamiaceae | Monotypic; Cuban endemic; cork palm |
| [*Stangeria*](encyclopedia/cycads/stangeria.json) | Stangeriaceae | Monotypic; fern-like leaves; South Africa |
| [*Bowenia*](encyclopedia/cycads/bowenia.json) | Stangeriaceae | Only cycad with bipinnate leaves; Australian endemic |

---

## How to Use These Templates

Each JSON file is a **fill-in template**. Fields marked `"[FILL IN]"` are placeholders awaiting encyclopedic content. The schema at [`schema/plant-entry.schema.json`](schema/plant-entry.schema.json) defines every available field and its expected data type.

### Adding a new genus entry

1. Copy the closest existing genus JSON file.
2. Update `"id"`, `"name"`, `"scientific_name"`, and `"taxonomy"` fields.
3. Replace all `"[FILL IN]"` strings with verified encyclopedic content.
4. Validate against the schema before committing.

### Adding a new category

1. Create a new directory under `encyclopedia/`.
2. Copy `template.json` from the nearest existing category.
3. Add a `README.md` following the cycads category overview as a model.

---

## Schema Overview

Key fields defined in [`schema/plant-entry.schema.json`](schema/plant-entry.schema.json):

| Field | Description |
|---|---|
| `id` | Unique entry identifier |
| `type` | Taxonomic rank (`genus`, `species`, `category`, …) |
| `name` | Common name |
| `scientific_name` | Latin scientific name |
| `taxonomy` | Full classification (kingdom → genus) |
| `description` | Lead summary paragraph |
| `conservation_status` | IUCN status and notes |
| `distribution` | Native range and habitat |
| `morphology` | Physical characteristics |
| `ecology` | Pollination, dispersal, symbioses |
| `uses` | Cultural, food, medicinal, horticultural, economic |
| `cultivation` | Growing guidance |
| `notable_species` | Curated species list |
| `gallery` | Image placeholders |
| `references` | Bibliographic citations |
| `external_links` | Web resources |
| `categories` | Encyclopedic tags |

---

*This encyclopedia is a work in progress. All entries marked `[FILL IN]` require verified content before publication.*
