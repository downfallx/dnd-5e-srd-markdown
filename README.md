# D&D 5e SRD 5.2.1 Markdown (2024) - Complete 5th Edition Reference

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![D&D 5e 2024](https://img.shields.io/badge/D%26D%205e-2024%20(5.2.1)-red.svg)](https://www.dndbeyond.com/)
[![Format](https://img.shields.io/badge/format-markdown-blue.svg)](https://commonmark.org/)

The complete **D&D 5e (2024) System Reference Document 5.2.1** converted to clean, developer-friendly Markdown format. Perfect for developers, content creators, and DMs who need programmatic access to official **Dungeons & Dragons 5th Edition** rules. Includes all 12 classes, 500+ spells, 400+ monsters, and complete D&D 5e gameplay rules.

## What is This?

The **D&D 5e (2024) SRD 5.2.1** is the official rules reference released by Wizards of the Coast under the Creative Commons Attribution 4.0 International License. This repository provides the **entire Dungeons & Dragons 5th Edition SRD in Markdown format** instead of PDF, making it ideal for D&D 5e apps, character builders, spell databases, and virtual tabletops:

- **Machine-readable** - Easy to parse and integrate into applications
- **Version-controllable** - Track changes with Git
- **Developer-friendly** - Use in static site generators, documentation tools, or APIs
- **Searchable** - Find what you need with grep, GitHub search, or your IDE
- **Accessible** - Works with screen readers and text-to-speech tools

## Contents

The SRD is organized into focused markdown files for easy navigation:

| File                                           | Size  | Description                           |
| ---------------------------------------------- | ----- | ------------------------------------- |
| [character-creation.md](character-creation.md) | 51KB  | Character creation steps and overview |
| [character-origins.md](character-origins.md)   | 17KB  | Backgrounds and species               |
| [classes.md](classes.md)                       | 292KB | All 12 core classes with subclasses   |
| [equipment.md](equipment.md)                   | 71KB  | Weapons, armor, gear, and tools       |
| [feats.md](feats.md)                           | 7.5KB | Character feats and abilities         |
| [spells.md](spells.md)                         | 319KB | Complete spell list (A-Z)             |
| [magic-items.md](magic-items.md)               | 239KB | Magic items and artifacts             |
| [playing-the-game.md](playing-the-game.md)     | 64KB  | Core gameplay rules and mechanics     |
| [gameplay-toolbox.md](gameplay-toolbox.md)     | 50KB  | Advanced rules and optional systems   |
| [monsters.md](monsters.md)                     | 19KB  | Monster statistics overview           |
| [monsters-A-Z.md](monsters-A-Z.md)             | 506KB | Complete bestiary                     |
| [animals.md](animals.md)                       | 137KB | Animal statistics and companions      |
| [rules-glossary.md](rules-glossary.md)         | 72KB  | Conditions, actions, and terminology  |

**Total:** ~1.9MB of pure D&D 5e rules content

## Quick Start

### For Developers

```bash
# Clone the repository
git clone https://github.com/downfallx/dnd-5e-srd-markdown.git

# Use in your project
cp -r dnd-5e-srd-markdown ./src/data/srd
```

### For Static Site Generators

```javascript
// Example: Load spell data in a Next.js app
import fs from 'fs';
import path from 'path';

const spellsPath = path.join(process.cwd(), 'data/srd/spells.md');
const spellsMarkdown = fs.readFileSync(spellsPath, 'utf8');
```

### For VTT Development

Integrate official D&D rules directly into your Virtual Tabletop:

```typescript
// Parse classes for character creation
import { marked } from 'marked';
import classData from './srd/classes.md';

const parsedClasses = marked.parse(classData);
```

### For Obsidian/Notion Users

Simply copy the markdown files into your vault/workspace for a complete D&D reference library with full text search and linking.

## Use Cases

This repository is ideal for:

- 🎮 **Game Development** - Build D&D-based video games or VTTs
- 🤖 **AI Training** - Feed D&D rules to LLMs for game master bots
- 📱 **Mobile Apps** - Character builders and spell reference apps
- 📚 **Documentation Sites** - Create searchable D&D wikis
- 🔧 **API Development** - Backend data for D&D web services
- 📖 **Personal Reference** - Offline-first rules reference

## Features

### Clean Markdown Formatting

- Proper heading hierarchy (`#`, `##`, `###`)
- Markdown tables for stat blocks and data
- Consistent formatting across all files
- No vendor lock-in or proprietary formats

### Structured Data

Each file follows a consistent structure:

- Clear section headers
- Nested subsections for easy navigation
- Tables for game statistics
- Lists for features and abilities

### Search-Friendly

```bash
# Find all spells with "fire" in the name
grep -i "fire" spells.md

# Find all creatures with CR 10+
grep "**Challenge:**" monsters-A-Z.md | grep -E "1[0-9]|2[0-9]"

# List all Wizard spells
grep -A 5 "## Wizard Spells" classes.md
```

## Differences from PDF

### Advantages

- **No parsing required** - Already in a structured text format
- **Git-friendly** - See exactly what changed between versions
- **Portable** - Works on any device, no PDF reader needed
- **Customizable** - Easy to modify or extend for homebrew content
- **Linkable** - Deep link to specific sections on GitHub

### Conversion Notes

- Tables are formatted using GitHub-flavored markdown
- Stat blocks use consistent markdown formatting
- All content from the official SRD 5.2.1 is preserved
- No proprietary formatting or embedded fonts

## License

This work includes material taken from the System Reference Document 5.2.1 ("SRD 5.2.1") by Wizards of the Coast LLC and is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

**You are free to:**

- Share — copy and redistribute the material
- Adapt — remix, transform, and build upon the material for any purpose

**Under the following terms:**

- Attribution — You must give appropriate credit to Wizards of the Coast

The official SRD 5.2.1 can be found at [Wizards of the Coast's website](https://www.dndbeyond.com/).

## Attribution

Dungeons & Dragons, D&D, and their respective logos are trademarks of Wizards of the Coast LLC.

This repository contains material from the System Reference Document 5.2.1, which is © 2024 Wizards of the Coast LLC. Used under Creative Commons Attribution 4.0 International License.

## Contributing

Found a formatting issue or conversion error? Contributions are welcome!

### How to Contribute

1. Fork this repository
2. Create a feature branch (`git checkout -b fix/spell-formatting`)
3. Make your changes
4. Ensure markdown is properly formatted (use a linter like `markdownlint`)
5. Submit a pull request

### Guidelines

- Preserve all official content exactly as written
- Maintain consistent markdown formatting
- Use tables for stat blocks and data
- Add links between related sections where helpful
- Follow the existing heading hierarchy

## FAQ

### Is this official?

The content is official (SRD 5.2.1 from Wizards of the Coast), but the markdown conversion is community-maintained.

### Can I use this in my commercial project?

Yes! The Creative Commons Attribution 4.0 license allows commercial use. Just provide attribution to Wizards of the Coast.

### How is this different from other SRD repos?

- **Latest version**: Uses SRD 5.2.1 (2024 revision)
- **Clean formatting**: Carefully converted with consistent structure
- **Complete**: All SRD content included, organized by topic
- **Maintained**: Actively accepting improvements and corrections

### What's not included?

The SRD is a subset of the core D&D rules. Not included:

- Character creation options beyond those in the SRD
- Subclasses not in the SRD
- Setting-specific content (Forgotten Realms, Eberron, etc.)
- Adventure content and campaigns

For the complete rules, purchase the official Player's Handbook, Dungeon Master's Guide, and Monster Manual.

## Related Projects

Looking for more D&D development resources?

- [5e-database](https://github.com/bagelbits/5e-database) - D&D 5e API
- [5e-srd-api](https://github.com/5e-bits/5e-srd-api) - REST API for D&D 5e
- [open5e](https://github.com/open5e/open5e-api) - D&D 5e open-source API

## Support

- 🐛 **Found a bug?** [Open an issue](https://github.com/downfallx/dnd-5e-srd-markdown/issues)
- 💡 **Have a suggestion?** [Start a discussion](https://github.com/downfallx/dnd-5e-srd-markdown/discussions)
- ⭐ **Like this project?** Star the repo!

## Changelog

### 1.0.0 (2024)

- Initial release with complete SRD 5.2.1 content
- All files converted to markdown format
- Organized by topic for easy navigation

---

**Disclaimer:** This is an independent conversion of the official D&D 5.2.1 SRD. It is not affiliated with, endorsed by, or sponsored by Wizards of the Coast.
