# Skills

A collection of portable `SKILL.md` files: reusable instruction sets that tell an AI assistant how to handle a specific kind of task.

## Contents

| File | Skill name | Language | Description |
|------|------------|----------|-------------|
| [`SKILL.de.md`](SKILL.de.md) | `augsburg-heute` | Deutsch | City-information assistant for Augsburg, Germany: current, source-checked local events, news, transport and practical info. |

## About the Augsburg skill

The skill is a free, bilingual (German/English) city guide for people who live in, study in, work in, or visit Augsburg. It works like this:

1. **Ask first.** The assistant asks a short multiple-choice question about topics (culture, food and drink, outdoors and sport, family, city news and transport), the time window, and the output format.
2. **Search live.** It searches current sources, preferring official ones (City of Augsburg, Stadtwerke Augsburg, University of Augsburg, venues and organizers) and verifies dates, times, venues and prices on the source page.
3. **Return the Top 3.** It answers with the three best verified results, with direct source links, practical notes and a quick recommendation, as a text list, visual cards, or a dashboard.

Core rules: never invent events, times, prices or URLs; state clearly what could not be verified; respond in the user's language.

## Usage

A `SKILL.md` file does not provide internet access by itself. The host assistant needs web search or browsing tools for the live-information workflow to work. Without them, the skill falls back to clearly labelled, non-live background information.

To use a skill, add the file to a compatible assistant (for example as a Claude skill, where the `name` and `description` in the frontmatter control when it is triggered), then ask something like:

- "Was ist heute in Augsburg los?"
- "Finde kostenlose Veranstaltungen in Augsburg an diesem Wochenende."
- "Gib mir einen zweisprachigen Überblick für Augsburg."

## File format

Each skill is a Markdown file with YAML frontmatter:

```yaml
---
name: skill-name
description: When the assistant should use this skill.
---
```

followed by the instructions themselves.

## Maintainer

[@kcLin2708](https://github.com/kcLin2708)
