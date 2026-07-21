# Control Decks

**One object. Multiple decks.**

Control Decks gives humans a small, explicit interface for directing agent behavior. Each deck has its own job. Every compatible card can receive the same Working Object, add a result or annotation, and pass it to the next deck.

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
    <td><strong>Reality Check</strong><br>Verify targets, sources, and assumptions.</td>
  </tr>
</table>

## Cards compose across decks

```text
THINK PROPOSE → REALITY CHECK ASSUMPTIONS
```

A proposal becomes the Working Object. Reality Check annotates its assumptions without replacing the proposal.

```text
WORK ASK FIRST
→ THINK TO PLAN
→ REALITY CHECK TARGETS
→ WORK IMPLEMENT
→ THINK EXPLAIN
```

One object moves through planning, verification, guarded execution, and presentation. The user sees one useful final result, not five disconnected reports.

## The shared grammar

```text
Binding + Working Object + Active Controls
```

- `binding` chooses what the cards apply to.
- `control` activates, qualifies, or clears visible state.
- `operation` transforms, annotates, or acts on the object.
- `presentation` changes representation without changing substance.

Cards resolve in written order. The full stream is prevalidated before its first effect. No hidden reordering, hidden duration card, or implicit permission grant is allowed.

## Decks

| Repository | Current release | Purpose |
|---|---:|---|
| [Think It Through](https://github.com/control-decks/think-it-through) | `0.12.0` | Thinking operations, bindings, and presentation |
| [Work This Way](https://github.com/control-decks/work-this-way) | `0.2.0` | Session controls and implementation |
| [Reality Check](https://github.com/control-decks/reality-check) | `0.2.0` | Read-only verification annotations |
| [HACP](https://github.com/control-decks/human-agent-control-protocol) | Draft `0.3` · plugin `0.2.0` | Shared protocol and optional authoring plugin |

Each deck is an autonomous Codex and Claude Code plugin. HACP conformance is behavioral; the optional HACP skill helps explain, create, and audit decks but is never required to use one.

## Start here

- Want to think something through? Install [Think It Through](https://github.com/control-decks/think-it-through).
- Want to change how the agent works in this session? Install [Work This Way](https://github.com/control-decks/work-this-way).
- Want to verify a result before relying on it? Install [Reality Check](https://github.com/control-decks/reality-check).
- Want to build a compatible deck? Read [HACP Draft 0.3](https://github.com/control-decks/human-agent-control-protocol/blob/main/SPEC.md) or play `HACP AUTHOR CARD` and `HACP AUTHOR DECK`.

Created by [thevzion](https://github.com/thevzion).
