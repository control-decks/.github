# Control Decks

**One object. Multiple decks.**

Control Decks gives humans a small, explicit interface for directing agent behavior. Each deck has its own job. Every compatible card can receive the same Working Object, add a result or scoped annotation, and pass it to the next deck.

> **HACP — Human-Agent Control Protocol**  
> **Cards are the interface. Control is the protocol.**

<table>
  <tr>
    <td width="33%"><a href="https://github.com/control-decks/think-it-through"><img src="https://raw.githubusercontent.com/control-decks/think-it-through/main/assets/github-preview.jpg" alt="Think It Through"></a></td>
    <td width="33%"><a href="https://github.com/control-decks/work-this-way"><img src="https://raw.githubusercontent.com/control-decks/work-this-way/main/assets/github-preview.jpg" alt="Work This Way"></a></td>
    <td width="33%"><a href="https://github.com/control-decks/reality-check"><img src="https://raw.githubusercontent.com/control-decks/reality-check/main/assets/github-preview.jpg" alt="Reality Check"></a></td>
  </tr>
  <tr>
    <td><strong>Think It Through</strong><br>Explore, decide, plan, and explain.</td>
    <td><strong>Work This Way</strong><br>Set visible session controls and act.</td>
    <td><strong>Reality Check</strong><br>Verify sources, assumptions, and concrete targets.</td>
  </tr>
</table>

## Cards compose across decks

These are recipes, not dependencies between decks. Cards compose through HACP
kinds, predicates, traits, and annotations rather than foreign card IDs.

```text
THINK PROPOSE → REALITY CHECK ASSUMPTIONS → REALITY CHECK SOURCES
```

A proposal becomes the Working Object. Reality Check annotates its assumptions and supporting evidence without replacing the proposal.

```text
WORK ASK FIRST
→ THINK TO PLAN
→ REALITY CHECK SOURCES
→ WORK IMPLEMENT
→ THINK EXPLAIN
```

One object moves through planning, evidence checking, guarded execution, and presentation. The user sees one useful final result, not five disconnected reports.

## The shared grammar

```text
Binding + Working Object + Active Controls
```

- `binding` chooses what the cards apply to.
- `control` activates, qualifies, or clears visible state.
- `operation` transforms, annotates, or acts on the object.
- `presentation` changes representation without changing substance.

Cards resolve in written order. The full stream is prevalidated before its first effect. No hidden reordering, hidden duration card, or implicit permission grant is allowed.

## Install HACP once

The HACP plugin loads the shared Draft 0.4 payload when a session starts. Cards
remain explicit human commands; the agent cannot infer, invoke, or replay them.

```bash
# Codex
codex plugin marketplace add control-decks/human-agent-control-protocol
codex plugin add hacp@hacp

# Claude Code
claude plugin marketplace add control-decks/human-agent-control-protocol --scope user
claude plugin install hacp@hacp --scope user
```

Then install only the decks you want.

## Decks

| Repository | Current release | Purpose |
|---|---:|---|
| [Think It Through](https://github.com/control-decks/think-it-through) | `0.13.0` | Thinking operations, bindings, and presentation |
| [Work This Way](https://github.com/control-decks/work-this-way) | `0.3.0` | Session controls and implementation |
| [Reality Check](https://github.com/control-decks/reality-check) | `0.3.1` | Read-only verification annotations |
| [HACP](https://github.com/control-decks/human-agent-control-protocol) | Draft `0.4` · plugin `0.3.0` | Required session adapter and authoring plugin |

Each deck is an independent Codex and Claude Code plugin, but full HACP
conformance requires a compatible session adapter. The canonical HACP plugin
loads that payload once and also explains, creates, and audits cards.

## Start here

- Want to think something through? Install [Think It Through](https://github.com/control-decks/think-it-through).
- Want to change how the agent works in this session? Install [Work This Way](https://github.com/control-decks/work-this-way).
- Want to verify a result before relying on it? Install [Reality Check](https://github.com/control-decks/reality-check).
- Want to build a compatible deck? Read [HACP Draft 0.4](https://github.com/control-decks/human-agent-control-protocol/blob/main/SPEC.md) or play `HACP AUTHOR CARD` and `HACP AUTHOR DECK`.

Created by [thevzion](https://github.com/thevzion).
