# Netto-Radar – rules & privacy

Public files for the **Netto-Radar** browser extension (German net salary next to the gross salary in job ads).

| File | What it is |
|---|---|
| [`DATENSCHUTZ.md`](DATENSCHUTZ.md) | Privacy policy / Datenschutzerklärung (DE/EN) |
| [`regras.json`](regras.json) | Rules file the extension downloads every 12 hours from `https://raw.githubusercontent.com/andradetkx/netto-radar-regeln/main/regras.json` |

## Why a rules file?

Job sites change how they write salaries without notice. This file lets the extension adapt without a new store release — for example by learning a new word for "per year" or pausing support for one site while a fix is prepared.

**Data only, never code.** The extension accepts nothing but word lists, numbers and on/off switches, validates every field and silently ignores anything else. A broken or missing file simply means the built-in defaults are used. No personal data is sent when the file is downloaded.

## Fields

| Field | Purpose | Example |
|---|---|---|
| `formato` | Always `1`; any other value makes the extension ignore the file | `1` |
| `atualizado` | Date of the last change (YYYY-MM-DD) | `"2026-09-24"` |
| `desligado` | `true` pauses the extension everywhere (emergency brake) | `false` |
| `sites.stepstone` / `.indeed` / `.linkedin` / `.arbeitsagentur` / `.karriere` | `false` pauses one site. New sites cannot be added here — that needs a new version with the site permission | `"linkedin": false` |
| `leitor.naoSalario` | Extra words meaning "this euro amount is not a salary" | `["Umzugspauschale"]` |
| `leitor.salario` | Extra words confirming a salary | `["Grundvergütung"]` |
| `leitor.periodos.jahr` / `monat` / `woche` / `stunde` | Extra words for the pay period | `"jahr": ["jährl."]` |
| `leitor.mensalMin` / `mensalMax` | Plausible gross monthly range in € | `300` / `40000` |
| `leitor.faixaMaxRazao` | Ranges wider than this (max ÷ min) are ignored | `3` |
| `lugares.adicionar` / `lugares.remover` | Places outside Germany (`CH`, `AT`, `LI`, `X`) added or removed | `{"Pfäffikon": "CH"}` |
| `contato` | Address for "Report a problem"; `null` hides the button | `"…@…"` |

Words: 2–40 characters (letters, digits, space and `. / - ' €`), up to 100 per list, case-insensitive.

## Contact

mauezx@gmail.com
