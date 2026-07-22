# lisa-skill-repo

Claude Code plugin marketplace, managed with [ecp-skillman](https://ecp-skillman.itdo.at/).

## Install

### Claude Code

Add this marketplace in Claude Code:

```
/plugin marketplace add lisawlf/lisa-skill-repo
```

Then install a plugin:

```
/plugin install ecp-main@lisa-skill-repo
```

### Other agents

These skills also work outside Claude Code (Cursor, Codex, Copilot and others) via [Vercel Labs Skills](https://github.com/vercel-labs/skills):

```bash
npx skills@latest add lisawlf/lisa-skill-repo
```

## Plugins

Each plugin lists its skills with a summary, source, and license.

> | | |
> |---|---|
> | 🤖👤 | invoked either way: Claude can load it on its own, and you can call it with `/name` |
> | 🤖 | self-invoked by the agent only, hidden from the `/` menu |
> | 👤 | user-invoked only, Claude will not load it on its own |

### ecp-main · v0.1.2

_No description._

```
/plugin install ecp-main@lisa-skill-repo
```

**skills**

| Skill | Use | What it does | Source | License |
|---|---|---|---|---|
| [animation-vocabulary](plugins/ecp-main/skills/skills/animation-vocabulary) | 🤖👤 | Reverse-lookup glossary that turns a vague description of a web animation or motion effect into its exact term ("the bouncy thing when a popover opens" → Pop in; "the iOS rubber-band scroll" → Rubber-banding). Use when the user asks "what's it called when…", or describes a motion effect without knowing its name and wants the right word to prompt an AI or designer with. For naming an effect, not designing or building one. | [Source](https://github.com/emilkowalski/skills/tree/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/skills/animation-vocabulary) | [License](https://github.com/emilkowalski/skills/blob/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/LICENSE) |
| [apple-design](plugins/ecp-main/skills/skills/apple-design) | 🤖👤 | Apple's approach to interface design and fluid, physical motion, translated for the web. Use when building or reviewing gesture-driven UI, spring animations, drag/swipe/sheet interactions, momentum and interruptible transitions, translucent materials and depth, typography (optical sizing, tracking, leading), reduced-motion, or the design foundations (feedback, spatial consistency, restraint) behind Apple-style interfaces. | [Source](https://github.com/emilkowalski/skills/tree/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/skills/apple-design) | [License](https://github.com/emilkowalski/skills/blob/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/LICENSE) |
| [emil-design-eng](plugins/ecp-main/skills/skills/emil-design-eng) | 🤖👤 | This skill encodes Emil Kowalski's philosophy on UI polish, component design, animation decisions, and the invisible details that make software feel great. | [Source](https://github.com/emilkowalski/skills/tree/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/skills/emil-design-eng) | [License](https://github.com/emilkowalski/skills/blob/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/LICENSE) |
| [find-animation-opportunities](plugins/ecp-main/skills/skills/find-animation-opportunities) | 🤖👤 | Search a codebase or UI for places that don't animate but should, and reject everything that shouldn't. Read-only; it proposes motion with exact values, it does not implement it. Use when the user asks "what could be animated here?" or wants to "make this feel more alive". For fixing existing animations, use improve-animations or review-animations instead. | [Source](https://github.com/emilkowalski/skills/tree/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/skills/find-animation-opportunities) | [License](https://github.com/emilkowalski/skills/blob/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/LICENSE) |
| [improve-animations](plugins/ecp-main/skills/skills/improve-animations) | 🤖👤 | Survey a codebase's animation and motion code as a senior motion advisor, then produce a prioritized audit and self-contained implementation plans for other agents (or cheaper models) to execute. Read-only on source code — it plans improvements, it does not apply them. Use when the user asks to "improve the animations", "audit the motion", "make this app feel better", or wants a roadmap of animation fixes rather than a review of a single diff. | [Source](https://github.com/emilkowalski/skills/tree/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/skills/improve-animations) | [License](https://github.com/emilkowalski/skills/blob/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/LICENSE) |
| [pick-ui-library](plugins/ecp-main/skills/skills/pick-ui-library) | 👤 | Pick the right library for a given frontend task from a curated, opinionated list — numbers, OTP inputs, charts, command menus, virtualization, drag and drop, toasts, state, styling, and more. Only runs when explicitly invoked; it does not trigger on its own. | [Source](https://github.com/emilkowalski/skills/tree/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/skills/pick-ui-library) | [License](https://github.com/emilkowalski/skills/blob/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/LICENSE) |
| [review-animations](plugins/ecp-main/skills/skills/review-animations) | 👤 | Reviews animation and motion code against a high craft bar derived from Emil Kowalski's design engineering philosophy. Default to flagging; approval is earned. | [Source](https://github.com/emilkowalski/skills/tree/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/skills/review-animations) | [License](https://github.com/emilkowalski/skills/blob/f6f79ca1d8e9e2d82c8b90d7481b70ca66f4adfb/LICENSE) |

---

_Generated by [ecp-skillman](https://ecp-skillman.itdo.at/)._
