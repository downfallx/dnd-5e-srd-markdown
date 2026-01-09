# Contributing to D&D 5.2.1 SRD Markdown

Thank you for your interest in improving this resource! This repository serves the D&D developer community by providing the SRD in a clean, accessible format.

## How to Contribute

### Types of Contributions Welcome

1. **Bug Reports** - Found a formatting error or typo? Let us know!
2. **Formatting Improvements** - Better table structures, clearer headers, improved readability
3. **Internal Linking** - Add helpful links between related sections
4. **Documentation** - Integration guides, tutorials
5. **Scripts & Tools** - Parsers, validators, converters, or search tools

### Types of Changes NOT Accepted

- Changes to official SRD content (we must match the official WotC SRD exactly)
- Homebrew content (this is for official SRD only)
- Additions beyond the SRD scope
- Significant structural reorganization (keep files as-is for consistency)

## Contribution Process

### 1. Before You Start

- Check existing issues to avoid duplicates
- For major changes, open an issue first to discuss
- Read this guide completely

### 2. Making Changes

```bash
# Fork the repository on GitHub

# Clone your fork
git clone https://github.com/YOUR_USERNAME/dnd-5.2-srd-markdown.git
cd dnd-5.2-srd-markdown

# Create a feature branch
git checkout -b fix/spell-table-formatting

# Make your changes
# ... edit files ...

# Test your changes (see Testing section below)

# Commit with a clear message
git commit -m "Fix spell table formatting in spells.md"

# Push to your fork
git push origin fix/spell-table-formatting

# Open a pull request on GitHub
```

### 3. Pull Request Guidelines

**Title Format:**
- `Fix: [Brief description]` - For bug fixes
- `Improve: [Brief description]` - For enhancements
- `Add: [Brief description]` - For new features
- `Docs: [Brief description]` - For documentation

**Description Should Include:**
- What changed and why
- Which file(s) were affected
- Screenshots (if formatting/layout changed)
- Related issue number (if applicable)

**Example:**
```markdown
## Summary
Fix malformed table in spells.md causing rendering issues

## Changes
- Fixed alignment of spell level column in Wizard spell table
- Corrected missing pipe characters in rows 234-245

## Testing
- [x] Previewed in GitHub markdown renderer
- [x] Validated with markdownlint
- [x] Checked table renders correctly in VS Code

Fixes #42
```

## Testing Your Changes

### 1. Markdown Validation

Install and run markdownlint:

```bash
npm install -g markdownlint-cli

# Lint specific file
markdownlint spells.md

# Lint all files
markdownlint *.md
```

### 2. Preview Rendering

- Preview in your IDE (VS Code markdown preview)
- Check on GitHub by viewing your branch
- Test with your intended use case (parser, static site, etc.)

### 3. Check for Broken Links

If you added internal links, verify they work:

```bash
# Install markdown-link-check
npm install -g markdown-link-check

# Check links
markdown-link-check README.md
```

## Content Guidelines

### Preserving Official Content

The SRD content must remain unchanged from the official WotC release.

**DO:**
- Fix markdown formatting errors
- Improve table structure for better parsing
- Add missing markdown syntax
- Fix typos in markdown formatting (like incorrect header levels)

**DON'T:**
- Change official spell/monster names
- Modify statistics or game mechanics
- Add homebrew content
- Alter official rules text
- Remove official content

### Formatting Standards

**Headers:**
```markdown
# Main Title (H1) - One per file
## Section Header (H2)
### Subsection Header (H3)
#### Detail Header (H4)
```

**Tables:**
```markdown
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Data     | Data     | Data     |
```

- Use consistent column alignment
- Include header separator row
- Align pipes for readability (optional but preferred)

**Lists:**
```markdown
- Unordered list item
  - Nested item (2 spaces indent)

1. Ordered list item
2. Second item
```

**Emphasis:**
```markdown
*Italic* or _italic_
**Bold** or __bold__
***Bold and italic***
```

**Code:**
````markdown
Inline `code` uses backticks

```
Code blocks use triple backticks
```
````

**Links:**
```markdown
[Link text](https://example.com)
[Internal link](#section-header)
```

### Cross-Referencing

When adding internal links:

```markdown
See the [Spells](#spells) section for more information.

For stat blocks, refer to [monsters-A-Z.md](monsters-A-Z.md#goblin).
```

- Use relative links for files in same directory
- Use anchor links for sections within a file
- Test all links before submitting

## Commit Message Guidelines

Use clear, descriptive commit messages:

**Good:**
```
Fix table alignment in equipment.md
Add internal links between class features and spells
Improve monster stat block formatting
Update README with documentation improvements
```

**Bad:**
```
fix stuff
updates
changes
asdf
```

**Format:**
```
<type>: <short description>

<optional longer description>

<optional footer>
```

**Types:**
- `fix` - Bug fixes
- `improve` - Enhancements to existing content
- `add` - New features or content
- `docs` - Documentation changes
- `style` - Formatting changes (no content change)
- `refactor` - Restructuring without changing content
- `test` - Adding or updating tests
- `chore` - Maintenance tasks

## Code of Conduct

### Our Standards

- Be respectful and inclusive
- Welcome newcomers
- Focus on constructive feedback
- Respect differing viewpoints
- Accept constructive criticism gracefully

### Unacceptable Behavior

- Harassment or discrimination
- Trolling or insulting comments
- Publishing others' private information
- Other unprofessional conduct

## Questions?

- Open an issue with the "question" label
- Start a discussion in GitHub Discussions
- Check existing issues and discussions first

## Recognition

Contributors will be:
- Listed in CHANGELOG.md for significant contributions
- Mentioned in release notes
- Credited in project documentation

Thank you for helping make D&D more accessible to developers! 🎲

## License

By contributing, you agree that your contributions will be licensed under the same Creative Commons Attribution 4.0 International License that covers the project.
