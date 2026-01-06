---
name: huberman-notes
description: Create comprehensive study guides from Huberman Lab podcast episodes. Use when user mentions "Huberman", "Huberman Lab", "Andrew Huberman", episode numbers like "episode 123", "Dr. Huberman", or asks about neuroscience/health podcast episodes. Triggers on "Huberman episode", "summarize Huberman", "study guide for Huberman", "notes on Huberman", or any reference to specific Huberman Lab episodes.
---

# Huberman Lab Study Guide Skill

Creates detailed, actionable study guides from Huberman Lab podcast episodes - designed for mastery-oriented learning with concrete protocols and science-backed insights you can reference and apply.

## Core References

Load these as needed:
- **[Study Guide Template](references/study-guide-template.md)** - Structure for study notes
- **[Protocol Format](references/protocol-format.md)** - How to extract actionable protocols

## Transcript Sources (Priority Order)

1. **HubermanTranscripts.com** - Best quality AI transcriptions (Whisper-based)
   - URL pattern: `https://www.hubermantranscripts.com/`

2. **PodScript.ai** - Free searchable transcripts
   - URL: `https://podscript.ai/podcasts/huberman-lab-podcast/`

3. **Official Huberman Lab** - Episode details and show notes
   - URL: `https://www.hubermanlab.com/episode/{slug}`

4. **Podcast Notes** - Community summaries with key takeaways
   - URL: `https://podcastnotes.org/huberman-lab/`

5. **YouTube** - Video with auto-generated captions
   - Search: `Huberman Lab {episode title or number}`

## Execution Workflow

### Step 1: Identify the Episode

Parse user input to identify:
- **Episode number** (e.g., "episode 123", "#123")
- **Episode title** (e.g., "the dopamine episode", "sleep protocols")
- **Guest name** (e.g., "the Attia episode", "with Jocko")
- **Topic** (e.g., "the one about cold exposure")

If unclear, ask: "Which Huberman Lab episode? I can search by episode number, title, topic, or guest name."

### Step 2: Fetch Episode Information

Search and fetch from multiple sources in parallel:

```
1. WebSearch: "Huberman Lab {episode identifier} transcript"
2. WebSearch: "Huberman Lab {episode identifier} summary notes"
3. WebSearch: "Andrew Huberman {topic} protocols"
4. WebFetch: hubermanlab.com episode page for show notes
```

Extract:
- Full episode title and number
- Guest (if any)
- Original air date
- Episode duration
- Official show notes/timestamps
- Full transcript (from transcript sources)
- Scientific papers mentioned

### Step 3: Parse the Transcript

Analyze the full transcript to extract:

**Key Concepts:**
- Main scientific concepts explained
- Mechanisms (how things work in the brain/body)
- Research studies cited (author, journal, findings)

**Actionable Protocols:**
- Specific recommendations with exact parameters
- Timing, dosage, frequency details
- Cost-free vs. supplement-based options

**Tools & Techniques:**
- Behavioral tools (free)
- Supplements (with dosages and timing)
- Technologies mentioned

**Quotes:**
- Most impactful statements (verbatim)
- Memorable explanations

### Step 4: Cross-Reference (Optional)

If the user has an existing note system, search for related content:
- Previous Huberman episodes on related topics
- Existing notes on same subjects
- Related concepts that connect

### Step 5: Generate Study Guide

Create comprehensive study guide following the template in `references/study-guide-template.md`

Save to: `huberman/{episode-number}-{slug}.md`

Example: `huberman/123-optimize-dopamine.md`

### Step 6: Update Index

Add entry to `huberman/episode-index.md`:
```markdown
| # | Title | Topics | Date | Link |
|---|-------|--------|------|------|
| 123 | Optimize Dopamine | dopamine, motivation | 2024-01-15 | [[123-optimize-dopamine]] |
```

### Step 7: Return Summary

Provide in chat:
- Episode overview (2-3 sentences)
- Top 3-5 actionable protocols (the "do this" items)
- Key insight that was most surprising/valuable
- Link to saved study guide
- Offer to deep-dive on any protocol

## Study Guide Structure

See `references/study-guide-template.md` for full template. Key sections:

```markdown
# Huberman Lab #{number}: {Title}

## Quick Reference (TL;DR)
- 3-5 bullet key takeaways
- The "if you only remember one thing" insight

## Episode Info
- Guest, date, duration, links

## Core Concepts
- Scientific mechanisms explained simply

## Actionable Protocols
- Numbered protocols with exact parameters
- Categorized: Behavioral (free) vs Supplements

## Scientific Evidence
- Studies cited with findings

## Tools & Resources
- Products, apps, techniques mentioned

## Timestamps & Navigation
- Key moments for re-listening

## Related Episodes
- Other Huberman episodes on same topic

## Related Notes
- Links to related notes in user's system
```

## Output Guidelines

### Writing Style
- **Direct and actionable** - focus on "what to do"
- **Science-backed** - always note the evidence level
- **Specific parameters** - exact doses, times, frequencies
- **Beginner-friendly** - explain jargon when used
- **Mastery-oriented** - explain WHY protocols work, not just WHAT

### Protocol Format
For each protocol, include:
```markdown
### Protocol: {Name}

**What:** {One-line description}
**Why it works:** {Mechanism in simple terms}
**How to do it:**
1. {Step 1 with specific details}
2. {Step 2}
3. {Step 3}

**Parameters:**
- Timing: {when}
- Duration: {how long}
- Frequency: {how often}

**Evidence:** {Study or observation supporting this}
**Cost:** {Free / $ / $$ / $$$}
**Difficulty:** {Easy / Medium / Advanced}
```

### Supplement Format
```markdown
### Supplement: {Name}

**Purpose:** {What it does}
**Dosage:** {Amount and form}
**Timing:** {When to take}
**With/Without food:** {Guidance}
**Cycle:** {If applicable - e.g., "5 days on, 2 days off"}
**Interactions:** {What to avoid combining}
**Source mentioned:** {Brand or type if specified}
**Huberman takes this:** {Yes/No/Sometimes}
```

## Example Interaction

**User:** "Give me the study guide for Huberman episode 39 - the dopamine one"

**Skill executes:**
1. Searches for "Huberman Lab episode 39 dopamine transcript"
2. Fetches hubermanlab.com show notes
3. Fetches transcript from hubermantranscripts.com
4. Parses for protocols (cold exposure, fasting dopamine, etc.)
5. Generates study guide
6. Saves to `huberman/039-controlling-dopamine.md`
7. Updates episode-index.md

**Returns:**
> ## Huberman #39: Controlling Your Dopamine
>
> This episode covers the science of dopamine - not as a "pleasure chemical" but as a molecule of motivation and pursuit. Dr. Huberman explains how dopamine works, why modern life depletes it, and protocols to optimize your baseline.
>
> ### Top Protocols:
> 1. **Cold exposure** - 1-3 min cold shower for 250% dopamine increase lasting hours
> 2. **Dopamine stacking avoidance** - Don't layer stimulants (caffeine + music + pre-workout)
> 3. **Intermittent reward** - Celebrate wins randomly, not every time
> 4. **Morning light viewing** - 10-30 min sunlight to set dopamine baseline
>
> ### Key Insight:
> "The pleasure you derive from something is related to how much dopamine was in your system when you started." - Managing baseline dopamine is more important than chasing peaks.
>
> Full study guide saved to [[huberman/039-controlling-dopamine|039-controlling-dopamine]]
>
> Want me to deep-dive on cold exposure protocols or the dopamine stacking concept?

## Works Well With

This skill pairs naturally with:
- Research skills for deep-dives on scientific papers mentioned
- Explainer skills for neuroscience concepts
- Fitness/health tracking for implementing protocols

## Vault Structure

```
huberman/
├── episode-index.md          # Master list of all episodes
├── topic-index.md            # Episodes organized by topic
├── protocol-library.md       # All protocols in one place
├── supplement-guide.md       # All supplements mentioned
├── 001-introducing-huberman-lab.md
├── 039-controlling-dopamine.md
├── 123-optimize-sleep.md
└── ...
```

## Topic Categories

Tag episodes with these categories for topic-index.md:

| Category | Topics |
|----------|--------|
| Sleep | sleep, circadian, melatonin, adenosine |
| Focus | dopamine, ADHD, attention, caffeine |
| Fitness | exercise, muscle, recovery, cold/heat |
| Nutrition | fasting, supplements, gut health |
| Mental Health | anxiety, depression, trauma, stress |
| Neuroscience | brain, neurons, neuroplasticity |
| Performance | learning, memory, motivation |
| Hormones | testosterone, estrogen, cortisol, thyroid |
| Longevity | aging, healthspan, rapamycin |
| Relationships | attachment, love, social connection |

## Notes

- Always search for the most recent transcript source (episodes update)
- Include timestamps when available for easy re-listening
- Note when Huberman has updated his stance on something
- Flag protocols that require medical supervision
- Distinguish between "Huberman does this" vs "research suggests this"
