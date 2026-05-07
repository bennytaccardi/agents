# Brainstorming Facilitator — Claude Code Skill

A structured brainstorming facilitator skill for [Claude Code](https://docs.anthropic.com/en/docs/claude-code) that guides interactive ideation sessions using 60+ creative techniques across 10 categories.

## Features

- **60+ brainstorming techniques** across 10 categories: collaborative, creative, deep, structured, theatrical, wild, biomimetic, quantum, cultural, and introspective
- **Two session modes:**
  - **Quick mode** — 10-30 ideas, optimized for speed and immediate usefulness
  - **Deep mode** — 50-100+ ideas, multi-technique exploration for maximum divergence
- **Session documentation** — automatically saved as timestamped markdown files
- **Anti-bias protocol** — forces domain shifts every 10 ideas to prevent semantic clustering
- **Micro-file workflow** — step-by-step facilitation with user control at each stage

## Installation

Copy the `brainstorming/` folder into your Claude Code skills directory:

```bash
# Option 1: Clone and copy
git clone https://github.com/bennytaccardi/agents.git
cp -r agents/skills/brainstorming ~/.claude/skills/

# Option 2: Clone directly into skills
git clone https://github.com/bennytaccardi/agents.git /tmp/agents-skill
cp -r /tmp/agents-skill/skills/brainstorming ~/.claude/skills/
rm -rf /tmp/agents-skill
```

The skill auto-registers via `SKILL.md` — no further configuration needed.

## Usage

Invoke the skill in Claude Code with `/brainstorming`, optionally followed by your topic:

```
/brainstorming
/brainstorming new product ideas for our SaaS platform
/brainstorming ways to improve developer onboarding
```

The facilitator will guide you through:

1. **Session setup** — define topic, goals, and mode
2. **Technique selection** — choose a technique or let the AI recommend one
3. **Guided ideation** — structured idea generation with the selected technique
4. **Organization** — cluster, prioritize, and document results

Session output is saved to `brainstorming/brainstorming-session-YYYY-MM-DD-HHMM.md` in your working directory.

## Skill Structure

```
brainstorming/
├── SKILL.md                 # Skill metadata and entry point
├── workflow.md              # Workflow architecture and rules
├── template.md              # Session output template
├── brain-methods.csv        # 60+ techniques database
└── steps/
    ├── step-01-session-setup.md
    ├── step-01b-continue.md
    ├── step-02a-user-selected.md
    ├── step-02b-ai-recommended.md
    ├── step-02c-random-selection.md
    ├── step-02d-progressive-flow.md
    ├── step-03-technique-execution.md
    └── step-04-idea-organization.md
```

## Technique Categories

| Category | Examples |
|---|---|
| Collaborative | Yes And Building, Brain Writing, Role Playing |
| Creative | What If Scenarios, First Principles, Reverse Brainstorming |
| Deep | Five Whys, Morphological Analysis, Question Storming |
| Structured | SCAMPER, Six Thinking Hats, Mind Mapping |
| Theatrical | Time Travel Talk Show, Alien Anthropologist, Dream Fusion |
| Wild | Chaos Engineering, Pirate Code, Anti-Solution |
| Biomimetic | Nature's Solutions, Ecosystem Thinking |
| Quantum | Observer Effect, Entanglement Thinking |
| Cultural | Indigenous Wisdom, Fusion Cuisine, Mythic Frameworks |
| Introspective | Inner Child Conference, Shadow Work Mining, Values Archaeology |
