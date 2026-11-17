# AGi — Amazing Grace Infrastructure

> A modular project for developing Grace, her capabilities, and the tools used to understand and improve her.

[![Organization](https://img.shields.io/badge/Organization-AGi--Robot-967BB6?logo=github&logoColor=white)](https://github.com/AGi-robot)
[![Status](https://img.shields.io/badge/Status-experimental-orange.svg)](https://github.com/AGi-robot)
[![Development workspace](https://img.shields.io/badge/Workspace-OppaAI%2FAGi-76B900?logo=github&logoColor=white)](https://github.com/OppaAI/AGi)

---

## Repository map

Repositories are grouped by their role in Grace’s architecture. The groups describe responsibility, not dependency or maturity.

### Entity · `#entity`

Grace’s runtime and internal systems: identity, orchestration, memory, sensory input, and system integration.

| Repository | Role |
|---|---|
| [AIVA](https://github.com/AGi-robot/AIVA) | Grace’s current runtime, including chat, identity, recent conversation memory, and integration with the WebUI and canvas. |

### Capabilities · `#capability`

Tools Grace can use to create, perceive, or act.

| Repository | Role |
|---|---|
| [Canvas](https://github.com/AGi-robot/canvas) | Vector drawing actions, validation, and SVG rendering. |
| [Imaging](https://github.com/AGi-robot/imaging) | Image-related capabilities used by Grace. |

### Shared components

| Repository | Role |
|---|---|
| [Memory](https://github.com/AGi-robot/memory) | Shared memory interface and storage backends. |
| [Cypher](https://github.com/AGi-robot/cypher) | Shared ROS 2 messages and signal encoding. |

### Interfaces

| Repository | Role |
|---|---|
| [Telepathy](https://github.com/AGi-robot/telepathy) | Web console, chat interface, and Canvas Studio. |
| [Augmented Reality](https://github.com/AGi-robot/augmented-reality) | Android Unity app that places Grace in the room using ARCore. |

### Diagnostics · `#diagnostic`

Benchmarks and checks used to inspect behavior, compare models, and validate components.

| Repository | Role |
|---|---|
| [Scorecard](https://github.com/AGi-robot/scorecard) | Benchmark protocols, evaluation results, and model comparisons. |

Unit-test repositories and test suites belong in this group when they are maintained separately from the component they test. Tests stored inside AIVA, Canvas, or Imaging stay with their component.

## How the groups fit together

```text
Grace
├── Entity       AIVA, memory, sensory input, runtime systems
├── Capabilities Canvas and Imaging
├── Shared       Memory and Cypher
├── Interfaces   Telepathy and Augmented Reality
└── Diagnostics  Scorecard and cross-component evaluation
```

The entity hosts and coordinates Grace’s behavior. Capabilities provide functions she can call. Diagnostics help evaluate her behavior and the models and components she uses.

### Project status
AGi is under active development. Repository descriptions and benchmark results document what has been implemented; planned model configurations and future capabilities should be treated as plans until they are integrated and evaluated.

Built in beautiful British Columbia, Canada.
