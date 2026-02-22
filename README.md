# Epistemic Architect — Claude Skill

A Claude skill that pressure-tests any business idea or concept through a
three-stage prompt chain: strip assumptions → build a grounded strategy →
simulate how your audience will actually react.

---

## What it does

Most business thinking starts from hidden assumptions. This skill runs three
analytical perspectives in sequence, each feeding into the next, to expose bad
premises before they become bad decisions.

**Stage 1 — The Epistemic Architect**
A cognitive scientist persona conducts a Socratic interrogation of your concept.
It asks hard questions about your sources of knowledge, hidden premises, and
counterfactuals, then outputs a structured **Reality Check Report** (what you
assume vs. what's actually defensible).

**Stage 2 — The Alien Collaborator**
A "Xenolinguist Strategist" takes the Reality Check and builds an execution plan,
flagging every section where it's making a "best guess." It also names the one
Blind Spot question you must answer before moving forward.

**Stage 3 — The Theory of Mind Simulator**
Claude adopts the persona of your target audience member — tired, busy, and
sceptical — and reacts to the strategy in real time: gut reaction, friction point,
and verdict on whether they'd act on it.

The result is a single conversation that takes you from vague idea to a
stress-tested plan with a clear next step.

---

## Installation

### Claude Code

Place this folder in your Claude Code skills directory:

```bash
# User-level (available in all projects)
~/.claude/skills/epistemic-architect/

# Project-level (available in this project only)
.claude/skills/epistemic-architect/
```

### Claude.ai (Cowork / Claude desktop)

Upload the skill folder via **Settings → Skills → Add custom skill**, or place
the folder at:

```
~/Library/Application Support/Claude/skills/epistemic-architect/   # macOS
%APPDATA%\Claude\skills\epistemic-architect\                        # Windows
```

### Via plugin marketplace (Claude Code)

```bash
# If published as a plugin, install with:
/plugin install epistemic-architect
```

---

## Usage

Once installed, trigger the skill with any of the following:

- `"Run the Epistemic Architect on my idea: [your concept]"`
- `"Pressure-test this concept: [your concept]"`
- `"I have a business idea I want to validate"`
- `"Help me think through this: [your concept]"`
- `"Run the three-prompt chain on [your concept]"`

Claude will ask for your concept if you haven't provided one, then run all three
stages automatically without pausing.

---

## Example

**Input:** `"I want to start a newsletter for dentists."`

**Stage 1 output (excerpt):**
> *Hidden Assumption:* All dentists are one market.
> *Actual Reality:* The dental market is highly segmented: solo vs. group, general vs. specialty. You must pick one segment and defend why you serve them better.

**Stage 2 output (excerpt):**
> *The Blind Spot:* "Which segment of dentists are you building for, and what is the one problem you are solving that is acute enough they will read something from an unknown sender?"

**Stage 3 output (excerpt):**
> *The Verdict:* I do not subscribe. You hooked me with a real problem, then asked for my email without proof. If you'd included one sample issue and a two-sentence bio, I would have clicked.

---

## The chain in one diagram

```
Your idea
    │
    ▼
[Stage 1] Epistemic Architect
    → Socratic interrogation
    → Reality Check Report
    │
    ▼
[Stage 2] Alien Collaborator
    → Gap analysis + execution plan
    → Flags every "best guess"
    → Names the Blind Spot
    │
    ▼
[Stage 3] Theory of Mind Simulator
    → Target audience reaction
    → Gut reaction, friction, verdict
    │
    ▼
Next Steps (2–3 concrete actions)
```

---

## Files

```
epistemic-architect/
├── SKILL.md              Claude instructions (required)
├── README.md             This file
├── LICENSE               Apache 2.0
└── references/
    └── original-prompts.md   Source prompts with attribution
```

---

## Attribution

The three-stage prompt structure was designed by
[God of Prompt](https://godofprompt.beehiiv.com/p/your-prompts-are-broken)
and is based on concepts from cognitive science and epistemology, including
Theory of Knowledge, First Principles thinking, and Theory of Mind.

This skill packages those prompts into a Claude-native sequential chain.

---

## License

Apache 2.0 — see [LICENSE](LICENSE).
