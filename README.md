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

<details>
<summary><strong>Other agents</strong> (Cursor, Codex, Copilot, Antigravity, OpenCode, and others)</summary>

**Copy the skills once** with [Vercel Labs Skills](https://github.com/vercel-labs/skills):

```bash
npx skills@latest add lisawlf/lisa-skill-repo
```

Or serve them live over MCP with [ecp-bridge](https://www.npmjs.com/package/ecp-bridge). Skills stay in this repo and auto-update whenever it changes, with no reinstall needed:

```json
{
  "mcpServers": {
    "ecp-bridge": {
      "command": "npx",
      "args": [
        "-y",
        "ecp-bridge",
        "lisawlf/lisa-skill-repo",
        "ecp-main"
      ]
    }
  }
}
```

Add that to your MCP client config. The final argument is optional: omit it to serve every plugin in the marketplace, or pass a comma-separated subset as shown.

</details>

## Plugins

Each plugin lists its skills with a summary, source, and license.

> | | |
> |---|---|
> | 🤖👤 | invoked either way: Claude can load it on its own, and you can call it with `/name` |
> | 🤖 | self-invoked by the agent only, hidden from the `/` menu |
> | 👤 | user-invoked only, Claude will not load it on its own |

### ecp-main · v0.1.4

_No description._

```
/plugin install ecp-main@lisa-skill-repo
```

| Skill | Use | What it does | Source | License |
|---|---|---|---|---|
| [https-github-com-emilkowalski-skills](plugins/ecp-main/skills/https-github-com-emilkowalski-skills) | 🤖👤 | Describe when Claude should use this skill. | - | - |
| [humanizer](plugins/ecp-main/skills/humanizer) | 🤖👤 | Remove signs of AI-generated writing from text. Use when editing or reviewing text to make it sound more natural and human-written. Based on Wikipedia's comprehensive "Signs of AI writing" guide. Detects and fixes patterns including: inflated symbolism, promotional language, superficial -ing analyses, vague attributions, em dash overuse, rule of three, AI vocabulary words, passive voice, negative parallelisms, and filler phrases. | [Source](https://github.com/blader/humanizer/tree/523374dee72d67c7b2b5f858ea0094ffda49c3ac) | [License](https://github.com/blader/humanizer/blob/523374dee72d67c7b2b5f858ea0094ffda49c3ac/LICENSE) |

**plugins/ecp-chat-skills/skills**

| Skill | Use | What it does | Source | License |
|---|---|---|---|---|
| [caveman](plugins/ecp-main/skills/plugins/ecp-chat-skills/skills/caveman) | 👤 | Ultra-compressed communication mode. Use when user says "caveman mode" or invokes /caveman. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-chat-skills/skills/caveman) | [License](https://github.com/ari-ayvazyan/AISkills/blob/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-chat-skills/skills/caveman/LICENSE.txt) |
| [edit-article](plugins/ecp-main/skills/plugins/ecp-chat-skills/skills/edit-article) | 👤 | Edit and improve articles by restructuring sections, improving clarity, and tightening prose. Use when user wants to edit, revise, or improve an article draft. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-chat-skills/skills/write-article) | - |
| [formatted-summary](plugins/ecp-main/skills/plugins/ecp-chat-skills/skills/formatted-summary) | 👤 | Summarizes texts in well digestible way | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-chat-skills/skills/formatted-summary) | - |
| [grilling](plugins/ecp-main/skills/plugins/ecp-chat-skills/skills/grilling) | 👤 | Grill the user relentlessly about a plan, decision, or idea. Use when the user wants to stress-test their thinking, or uses any 'grill' trigger phrases. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-chat-skills/skills/grilling) | [License](https://github.com/ari-ayvazyan/AISkills/blob/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-chat-skills/skills/grilling/LICENSE) |
| [micro-spec](plugins/ecp-main/skills/plugins/ecp-chat-skills/skills/micro-spec) | 👤 | Turn a project idea into a minimal, on-point SPEC.md (caveman style — least text, max info). Use when the user runs /micro-spec or asks to spec out / document a project idea. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-chat-skills/skills/handoff-micro-spec) | - |

**plugins/ecp-code-agent-skills/skills**

| Skill | Use | What it does | Source | License |
|---|---|---|---|---|
| [architecture-decisions](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/architecture-decisions) | 🤖👤 | ALWAYS Execute this skills before deciding any technical/architectural matter, to avoid reintroducing already-solved issues. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/architecture-decisions) | - |
| [diagnosing-bugs](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/diagnosing-bugs) | 🤖👤 | Diagnosis loop for hard bugs and performance regressions. Use when the user says "diagnose"/"debug this", or reports something broken/throwing/failing/slow. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/diagnosing-bugs) | - |
| [tdd](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/tdd) | 🤖👤 | Test-driven development. Use when the user wants to build features or fix bugs test-first, mentions "red-green-refactor", or wants integration tests. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/tdd) | - |
| [teach](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/teach) | 👤 | Teach the user a new skill or concept, within this workspace. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/teach) | - |

**plugins/ecp-code-agent-skills/skills/meta**

| Skill | Use | What it does | Source | License |
|---|---|---|---|---|
| [create-agent-skills](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/meta/create-agent-skills) | 👤 | Expert guidance for Claude Code Skills. Use when working with SKILL.md files, authoring new skills, improving existing skills, or understanding skill structure. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/meta/create-agent-skills) | - |
| [init-agent-project](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/meta/init-agent-project) | 👤 | Bootstraps a project for AI-agent usage in any agent. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/meta/init-agent-project) | - |
| [mcp-builder](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/meta/mcp-builder) | 👤 | Guide for creating high-quality MCP (Model Context Protocol) servers that enable LLMs to interact with external services through well-designed tools. Use when building MCP servers to integrate external APIs or services, whether in Python (FastMCP) or Node/TypeScript (MCP SDK). | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/meta/mcp-builder) | - |

**plugins/ecp-code-agent-skills/skills/planning**

| Skill | Use | What it does | Source | License |
|---|---|---|---|---|
| [codebase-design](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/planning/codebase-design) | 🤖👤 | Shared vocabulary for designing deep modules. Use when the user wants to design or improve a module's interface, find deepening opportunities, decide where a seam goes, make code more testable or AI-navigable, or when another skill needs the deep-module vocabulary. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/planning/codebase-design) | - |
| [improve-codebase-architecture](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/planning/improve-codebase-architecture) | 👤 | Scan a codebase for deepening opportunities, present them as a visual HTML report, then grill through whichever one you pick. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/planning/improve-codebase-architecture) | - |

**plugins/ecp-code-agent-skills/skills/web**

| Skill | Use | What it does | Source | License |
|---|---|---|---|---|
| [favicon-generator](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/web/favicon-generator) | 👤 | Generate professional-quality favicons. Trigger when you need favicons, app icons, or browser tab icons. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/web/favicon-generator) | - |
| [og-image-creator](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/web/og-image-creator) | 👤 | Smart OG image generation that studies your codebase, understands routes and brand identity, then creates contextually appropriate Open Graph images using Playwright and React components. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/web/og-image-creator) | - |
| [seo-optimizer](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/web/seo-optimizer) | 👤 | Comprehensive SEO optimization for web applications. Use when asked to improve search rankings, add meta tags, create structured data, generate sitemaps, optimize for Core Web Vitals, or analyze SEO issues. Works with Next.js, Astro, React, and static HTML sites. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/web/seo-optimizer) | - |

**plugins/ecp-code-agent-skills/skills/web/planning**

| Skill | Use | What it does | Source | License |
|---|---|---|---|---|
| [color-architect](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/web/planning/color-architect) | 👤 | Generates strategic color palettes. Use when creating or updating app color schemes, theming, or brand colors. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/web/planning/color-architect) | - |
| [generate-app-names](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/web/planning/generate-app-names) | 👤 | Generates strategic product and application names using linguistic engineering. Trigger when invoked with /generate-app-names | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/web/planning/generate-app-names) | - |
| [minimalist-web-design](plugins/ecp-main/skills/plugins/ecp-code-agent-skills/skills/web/planning/minimalist-web-design) | 👤 | Designs and reviews minimalist, editorial-feeling web interfaces to a 2026 standard — distinctive layouts, extreme typographic hierarchy, restrained-but-bold color, strict performance budgets, and motion/SVG developer handoff. Use when designing a landing page or marketing site, auditing an existing design for generic "visual recycling," or preparing animated SVGs (e.g. GSAP DrawSVG) for developer handoff. | [Source](https://github.com/ari-ayvazyan/AISkills/tree/28487061266dbdfb193e2a45e62fa82b9746b661/plugins/ecp-code-agent-skills/skills/web/planning/minimalist-web-design) | - |

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
