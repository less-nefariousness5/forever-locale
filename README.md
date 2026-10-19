# Forever Locale

Language packs for **Forever Tank** and **Forever Questing** (WoW Forever). The addons download a pack the
first time a player picks its language in Appearance, save it under `scripts_data/forever_locale/<code>/`,
and update it when this repo has a newer version.

| Code | Language |
|---|---|
| deDE | Deutsch |
| frFR | Français |
| esES | Español |
| ptBR | Português (Brasil) |
| itIT | Italiano |

English and Simplified Chinese ship inside the addons and have no pack here.

## Contents

Plain text, never code. Each line is tab-separated; `\\`, `\t` and `\n` are escaped.

- `manifest.tsv`: `code  version  file  size`. The addons accept a file only at exactly this size.
- `<code>/ui.tsv`: interface strings, `English  translation`.
- `<code>/templates.tsv`: dynamic phrases, `Lua pattern  translation`.
- `<code>/guide_<x>.tsv`: guide steps, `source hash  English  translation`, split by the hash's first hex digit.

Names (NPCs, quests, items, spells, zones) stay in English to match the English game client.

## Notes

The translations are machine-generated and not yet reviewed by native speakers; corrections are welcome.
The guide text comes from RestedXP guides and is published with permission.
Packs are built by `tools/forever_guides/locale_pack.py` in the addon repository.
