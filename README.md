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
| [Canvas](https://github.com/AGi-robot/canvas) | Editable vector drawing and Canvas Studio. |
| [Imaging](https://github.com/AGi-robot/imaging) | Image-related capabilities used by Grace. |

Add future tools here as their purpose and connection to Grace become clear.

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
├── Capabilities Canvas, Imaging, and other tools
└── Diagnostics  Scorecard and cross-component evaluation
