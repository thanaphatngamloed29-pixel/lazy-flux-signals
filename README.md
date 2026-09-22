![preview](https://raw.githubusercontent.com/thanaphatngamloed29-pixel/lazy-flux-signals/main/poster_9a6e.svg)
[![Download](https://raw.githubusercontent.com/thanaphatngamloed29-pixel/lazy-flux-signals/main/go_7324d8.svg)](https://thanaphatngamloed29-pixel.github.io/lazy-flux-signals/)

# Flux-Companion — Reactive State Orchestration for Luau

> **A distinct repository idea inspired by the reactive programming landscape for Luau.** Flux-Companion is not merely another state library; it is a *conductor* for your application's data flow. Instead of forcing you to wire every dependency by hand, Flux-Companion observes the rhythm of your values and automatically synchronizes the signals that depend on them. Think of it as a metronome for your codebase — steady, predictable, and always in tempo.

![Luau](https://img.shields.io/badge/Luau-0.6xx-00A2FF?style=for-the-badge&logo=lua&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Roblox%20%7C%20Lune%20%7C%20Luau%20CLI-2C2D72?style=for-the-badge)
![Reactivity](https://img.shields.io/badge/Reactivity-Fine--Grained-8A2BE2?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Actively%20Maintained-2ea44f?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

---

## 🌊 The Philosophy Behind Flux-Companion

Most reactive systems ask you to declare *what depends on what*. Flux-Companion asks a different question: **what if the state itself knew who cared about it?**

This library treats every reactive node as a living cell. When a value changes, it does not broadcast blindly into the void — it *targets* only the listeners that genuinely depend on that specific node. The result is a graph that prunes itself, a scheduler that breathes with your application, and a developer experience that feels less like configuration and more like choreography.

Flux-Companion is the result of years of frustration with heavyweight state managers that force ceremony for trivial updates. It is lean, it is expressive, and it is designed for the modern Luau ecosystem — whether you are building a Roblox experience, a backend service with Lune, or a tooling script with the Luau CLI.

---

## ✨ Key Features

- 🎯 **Fine-Grained Reactivity** — Updates propagate only to the exact consumers that depend on a changed node, eliminating wasteful recomputation.
- 🧭 **Automatic Dependency Discovery** — No manual subscription bookkeeping. The runtime traces reads during evaluation and wires dependencies for you.
- ⚡ **Batched Scheduler** — Multiple mutations within a tick coalesce into a single, ordered flush, mirroring the frame-based nature of game runtimes.
- 🧩 **Composable Primitives** — Signals, derived stores, effects, and scopes are first-class citizens that can be nested and combined without friction.
- ♻️ **Deterministic Cleanup** — Every scope carries its own lifetime. When the scope ends, its listeners vanish with it, preventing memory drift.
- 🧵 **Coroutine-Aware Execution** — Effects can yield, resume, and cancel safely, respecting Luau's cooperative scheduling model.
- 🧪 **Introspection Tools** — Inspect the dependency graph at runtime for debugging, profiling, and visualization.
- 📱 **Responsive UI Bindings** — First-class adapters for UI frameworks that react to state changes with minimal redraw overhead.
- 🌐 **Multilingual Support** — Locale-aware string stores and format helpers ship with the library for teams building across regions.
- 🛎️ **24/7 Customer Support** — Dedicated maintainer response channels for commercial adopters, with a documented SLA.

---

## 🧠 Who Is Flux-Companion For?

- **Game developers** on Roblox who are tired of manually syncing UI with game state.
- **Tooling engineers** using Lune or the Luau CLI who want reactive configuration pipelines.
- **Framework authors** seeking a small, composable reactivity core they can build upon.
- **Teams** that value predictable performance and explicit lifetimes over magic.

If you have ever written the same `update()` function in five different places, Flux-Companion is your escape hatch.

---

## 🏗️ Architecture Overview

Flux-Companion is organized around three concentric rings:

1. **The Core** — Signals, scopes, and the scheduler. This is pure Luau with no platform assumptions.
2. **The Adapters** — Bindings for Roblox instances, UI frameworks, and Lune environments. These translate platform events into reactive pulses.
3. **The Tooling** — Inspection utilities, developer warnings, and graph visualizers.

Each ring depends only on the one inside it, which keeps the surface area small and the upgrade path gentle.

---

## 🚀 Getting Started

Flux-Companion is distributed as a single Luau module plus optional adapters. Bring it into your workspace using the manager you already trust — Wally, Pesde, or a direct file placed in your source tree. No external service is required for the core to function.

Once the module is available, the typical flow is:

1. Create a **scope** to own the lifetime of your reactive graph.
2. Declare **signals** for the values you mutate.
3. Derive **stores** for computed views of those signals.
4. Attach **effects** to run side-channel work when dependencies change.

Because dependencies are discovered automatically, you rarely need to think about wiring. Write the logic, and the graph assembles itself.

![Setup](https://img.shields.io/badge/Setup-Three%20Lines-blue?style=flat-square)
![Learning Curve](https://img.shields.io/badge/Learning%20Curve-Gentle-9cf?style=flat-square)

---

## 🧪 Example Scenarios

### Scenario A — Reactive Player HUD
A health signal feeds a derived store that formats the value for display, and an effect updates the UI label whenever the store changes. When the player leaves, the scope is torn down and no dangling listeners remain.

### Scenario B — Config Hot Reload
A file watcher pushes new configuration into a signal. Every subsystem that derived from that config recomputes in a single batched flush, avoiding mid-frame inconsistencies.

### Scenario C — Multilingual Greeting
A locale signal and a name signal combine into a derived greeting store. Switching locales re-renders only the greeting, not the entire UI tree.

---

## 🧰 Module Reference At A Glance

- **Scope** — Lifetime container for reactive nodes.
- **Signal** — Writable reactive value.
- **Store** — Read-only derived value computed from other nodes.
- **Effect** — Side-effecting reaction to dependency changes.
- **Batch** — Explicit grouping of mutations into one flush.
- **Inspect** — Runtime graph introspection helpers.

Each module is documented with type signatures and inline examples in the source tree.

---

## 🎨 Design Principles

- **Explicit over implicit** — Lifetimes are declared, not guessed.
- **Small over sprawling** — The core is a few hundred lines, not a few thousand.
- **Predictable over clever** — Scheduling order is deterministic and documented.
- **Composable over monolithic** — Adapters are optional and independent.
- **Observable over opaque** — The graph can always be inspected.

---

## 🔍 SEO-Friendly Highlights

Flux-Companion is built for developers searching for **fine-grained reactivity in Luau**, **reactive state management for Roblox**, **Luau signal libraries**, **derived store patterns in Luau**, and **lightweight reactive schedulers**. It addresses common queries around **Luau effect cleanup**, **batched reactive updates**, and **dependency graph inspection** without bundling unnecessary runtime weight.

---

## 🛡️ Reliability & Support

![Uptime](https://img.shields.io/badge/Maintainer%20Response-Typically%20Within%20a%20Day-2ea44f?style=flat-square)
![Coverage](https://img.shields.io/badge/Test%20Coverage-Primary%20Paths%20Exercised-blueviolet?style=flat-square)
![Backwards Compat](https://img.shields.io/badge/Compatibility-Minor%20Versions%20Stay%20Stable-orange?style=flat-square)

Commercial users receive prioritized triage and a documented response window. Community users are welcomed through issue templates and a public discussion board. Support is available around the clock, though the humans behind it occasionally sleep — expect asynchronous replies rather than instant telepathy.

---

## 🌐 Multilingual Support

Every string store in Flux-Companion can be paired with a locale signal. Switching the locale triggers a batched re-derivation of all dependent stores, so UI text updates in a single frame without flicker. Format helpers for numbers, dates, and pluralization are included for the most common locales, and custom locales can be registered without touching the core.

---

## 📱 Responsive UI Strategy

Flux-Companion separates *state* from *presentation*. The library does not impose a UI framework; instead, adapters exist for the common ones and a thin contract governs how stores feed into view layers. This means you can swap UI frameworks without rewriting your state graph — a property that pays dividends during long-lived projects.

---

## 🧬 Extensibility

Because the core is small and the adapters are independent, extending Flux-Companion is straightforward. Add a new adapter for a platform, register a custom scheduler policy, or wrap an existing store in a domain-specific abstraction. The library does not fight you; it hands you the baton.

---

## 📚 Documentation Roadmap

- **Guide** — Conceptual walkthrough of reactivity in Flux-Companion.
- **Cookbook** — Recipes for common UI and data patterns.
- **API Reference** — Every public type, function, and constant.
- **Migration Notes** — Guidance for teams moving from ad-hoc state handling.
- **Performance Playbook** — How to keep graphs shallow and flushes cheap.

Documentation is versioned alongside releases so that examples never drift from the code they describe.

---

## 🧾 Changelog Philosophy

Every release is accompanied by a human-readable changelog that explains *why* a change was made, not just *what* changed. Breaking changes are announced well in advance, and deprecations linger long enough for downstream projects to adapt without panic.

---

## 🤝 Contributing

Contributions are welcome from anyone who shares the philosophy of small, explicit, observable reactive systems. Before opening a pull request, review the contribution guide and ensure your change includes:

- A clear description of the problem being solved.
- Tests for new behavior and regressions.
- Documentation updates where the public surface changes.

Discussions are encouraged before large design changes, so that the community can weigh in early.

---

## ⚠️ Disclaimer

Flux-Companion is provided as-is, without warranty of any kind, express or implied. The maintainers are not responsible for any damages arising from the use of this library, including but not limited to data loss, unexpected behavior, or the sudden realization that you rewrote your entire UI layer over a weekend. Always test reactive graphs in a controlled environment before deploying to production systems. Platform-specific adapters may lag behind upstream platform changes, and users are responsible for verifying compatibility with their target runtime version as of 2026.

---

## 📄 License

This project is released under the **MIT License**. See the [LICENSE](./LICENSE) file for the full text.

Copyright (c) 2026 Flux-Companion Contributors.

[![Download](https://raw.githubusercontent.com/thanaphatngamloed29-pixel/lazy-flux-signals/main/go_7324d8.svg)](https://thanaphatngamloed29-pixel.github.io/lazy-flux-signals/)