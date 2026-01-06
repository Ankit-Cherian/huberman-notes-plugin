# Huberman Notes Plugin for Claude Code

A Claude Code plugin that creates comprehensive study guides from Huberman Lab podcast episodes.

## Features

- **Structured Study Guides**: Generates detailed notes following a consistent template
- **Actionable Protocols**: Extracts specific, parameterized protocols (timing, dosage, frequency)
- **Scientific References**: Captures studies and evidence levels
- **Supplement Tracking**: Documents supplements with dosages, timing, and interactions
- **Episode Indexing**: Maintains organized episode and topic indexes

## Installation

```bash
claude /plugin install github:Ankit-Cherian/huberman-notes-plugin
```

## Usage

After installation, use the skill by mentioning Huberman Lab episodes:

```
"Give me study notes for Huberman episode 39 on dopamine"
"Summarize the Huberman episode with Dr. Attia"
"What are the sleep protocols from Huberman Lab?"
```

The skill will:
1. Search for transcripts and show notes
2. Extract key concepts and protocols
3. Generate a structured study guide
4. Save to your vault in `huberman/` folder

## Output Structure

Each study guide includes:
- **Quick Reference (TL;DR)** - Key takeaways
- **Core Concepts** - Scientific mechanisms explained
- **Actionable Protocols** - Step-by-step instructions with parameters
- **Supplement Protocols** - Dosages, timing, interactions
- **Scientific Studies** - Research citations
- **Timestamps** - For easy re-listening

## Vault Structure

The plugin expects/creates this structure:

```
huberman/
├── episode-index.md      # Master list of episodes
├── topic-index.md        # Episodes by topic
├── protocol-library.md   # All protocols
├── supplement-guide.md   # All supplements
└── {number}-{slug}.md    # Individual episode notes
```

## Configuration

### Save Location
By default, study guides save to `huberman/` in your current directory. You can customize this by modifying the skill's save path instructions after installation.

### Templates
The skill uses reference templates that you can customize:
- `references/study-guide-template.md` - Note structure
- `references/protocol-format.md` - Protocol formatting

### Note Linking
The templates use `[[wikilink]]` syntax compatible with Obsidian, Logseq, and similar tools. Adjust the link format in the templates if you use a different system.

## Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request

For bugs or feature requests, open an issue on GitHub.

## License

MIT
