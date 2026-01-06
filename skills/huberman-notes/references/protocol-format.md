# Protocol Format Reference

How to extract and format actionable protocols from Huberman Lab episodes.

---

## Protocol Types

### 1. Behavioral Protocols

Free actions you can take immediately.

**Template:**
```markdown
### Protocol: {Descriptive Name}

**Category:** {Sleep / Focus / Fitness / Stress / etc.}
**Cost:** Free
**Difficulty:** {Easy / Medium / Advanced}

**The 30-second version:**
{What to do in one paragraph}

**Why it works (the science):**
{Mechanism - what's happening biologically}
{Keep this accessible but accurate}

**Step-by-step:**
1. {Specific step with parameters}
2. {Next step}
3. {Final step}

**Parameters:**
| Aspect | Recommendation |
|--------|----------------|
| Timing | {When - be specific} |
| Duration | {How long each session} |
| Frequency | {How often} |
| Intensity | {If applicable} |

**Optimize it:**
- {Pro tip 1}
- {Pro tip 2}

**Common mistakes:**
- {What people get wrong}

**Evidence:**
- {Study or source}
- Evidence level: {Strong / Emerging / Anecdotal}

**Huberman's practice:**
"{What he personally does, if mentioned}"
```

---

### 2. Supplement Protocols

**Template:**
```markdown
### Supplement: {Compound Name}

**Purpose:** {Primary benefit}
**Category:** {Sleep / Focus / Performance / Recovery / etc.}

**Dosage & Timing:**
| Parameter | Recommendation |
|-----------|----------------|
| Dose | {Amount - range if applicable} |
| Form | {Specific form matters - e.g., Magnesium L-Threonate vs Glycinate} |
| Timing | {When to take} |
| With food | {Yes / No / Either} |
| Cycle | {Continuous / X on Y off} |
| Duration | {How long to try before assessing} |

**How it works:**
{Mechanism in simple terms}

**What to expect:**
- Onset: {How quickly you notice effects}
- Peak benefits: {Timeline}
- If it's working: {Signs of success}

**Interactions & Warnings:**
- Don't combine with: {Contraindications}
- Consult doctor if: {Conditions}
- Side effects: {Common issues}

**Quality markers:**
- Look for: {What indicates quality}
- Avoid: {Red flags}
- Brands mentioned: {If Huberman specified}

**Cost estimate:** {$ / $$ / $$$}

**Evidence level:** {Strong / Emerging / Anecdotal}

**Huberman's usage:**
{His personal protocol if mentioned}
```

---

### 3. Combination Protocols (Stacks)

When multiple interventions work together.

**Template:**
```markdown
### Stack: {Name - e.g., "Morning Focus Stack"}

**Goal:** {What this combination achieves}

**Components:**
1. **{Element 1}** - {Role in stack}
2. **{Element 2}** - {Role in stack}
3. **{Element 3}** - {Role in stack}

**Timing sequence:**
| Time | Action |
|------|--------|
| {Time 1} | {What to do} |
| {Time 2} | {What to do} |
| {Time 3} | {What to do} |

**Why stack them:**
{Synergy explanation}

**Don't combine with:**
{What to avoid}

**Difficulty:** {Easy / Medium / Advanced}
**Cost:** {Free / $ / $$ / $$$}
```

---

### 4. Environment Protocols

Setting up your physical space.

**Template:**
```markdown
### Environment: {Setting - e.g., "Optimal Sleep Environment"}

**Goal:** {What you're optimizing for}

**Setup checklist:**
- [ ] {Physical element 1}
- [ ] {Physical element 2}
- [ ] {Technology adjustment}

**Key parameters:**
| Factor | Target |
|--------|--------|
| Temperature | {Specific range} |
| Light | {Lux level or description} |
| Sound | {dB or description} |
| Other | {Relevant factors} |

**Products mentioned:**
- {Product} - {Purpose} - {Cost}

**DIY alternatives:**
- {Free/cheap option}
```

---

## Protocol Extraction Guidelines

### What Makes a Protocol

A protocol is NOT just information - it's actionable. Include something only if you can answer:
- **What exactly do I do?**
- **When do I do it?**
- **For how long?**
- **How will I know it's working?**

### Specificity Requirements

**Too vague (don't include):**
- "Get morning sunlight"
- "Take magnesium"
- "Do cold exposure"

**Specific enough (do include):**
- "View sunlight within 30-60 minutes of waking, for 10-30 minutes (longer on cloudy days), without sunglasses"
- "300-400mg Magnesium L-Threonate, 30-60 minutes before bed"
- "1-3 minutes cold water exposure (50-60°F), 1-3x per week, ideally in morning"

### Evidence Level Criteria

**Strong research:**
- Multiple randomized controlled trials
- Meta-analyses or systematic reviews
- Published in peer-reviewed journals
- Replicated findings

**Emerging research:**
- 1-2 studies with promising results
- Mechanistically sound but limited human data
- Active area of investigation

**Anecdotal:**
- Based on clinical observation
- Personal experience of experts
- Logical based on mechanisms but untested

**Theoretical:**
- Makes sense based on biology
- No direct studies on this application
- "Should work" but speculative

### Huberman's Personal Practice

Always note what Huberman personally does vs. what he recommends generally. Format:

> "I personally do X" - indicates his routine
> "The research suggests X" - indicates general recommendation
> "Some people find X helpful" - indicates individual variation

### Safety Flagging

Flag protocols that need extra caution:

```markdown
**Safety Note:** {Warning}
- Consult healthcare provider before: {Condition}
- Not recommended for: {Population}
- Stop if: {Warning signs}
```

---

## Common Protocol Categories

Use these tags for organizing:

| Category | Includes |
|----------|----------|
| `#sleep` | Sleep quality, duration, timing, disorders |
| `#focus` | Attention, concentration, ADHD, cognitive enhancement |
| `#energy` | Alertness, fatigue, caffeine, stimulants |
| `#stress` | Anxiety, cortisol, relaxation, resilience |
| `#mood` | Depression, emotional regulation, motivation |
| `#fitness` | Exercise, recovery, muscle, endurance |
| `#nutrition` | Fasting, diet, gut health, metabolism |
| `#hormones` | Testosterone, estrogen, thyroid, cortisol |
| `#cold` | Cold exposure, deliberate cold |
| `#heat` | Sauna, deliberate heat |
| `#light` | Light exposure, circadian, seasonal |
| `#breathing` | Breathwork protocols |
| `#supplements` | All supplement protocols |
| `#longevity` | Aging, healthspan, lifespan |

---

## Quality Checklist

Before including a protocol, verify:

- [ ] Specific parameters (dose/duration/frequency)
- [ ] Mechanism explained (why it works)
- [ ] Evidence level stated (how strong is the support)
- [ ] Huberman's personal use noted (if mentioned)
- [ ] Cost indicated (free/$/$$/$$$ )
- [ ] Difficulty rated (easy/medium/advanced)
- [ ] Safety considerations addressed
- [ ] Common mistakes listed
- [ ] Signs of success described
