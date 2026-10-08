# DakiKobo Kiro showcase

This repository is a challenge-oriented snapshot derived from the earlier
[`MORAWA-dev/dakikobo`](https://github.com/MORAWA-dev/dakikobo) project. The
agricultural application predates this repository. The Kiro configuration,
specification, hook, custom agent, MCP configuration, and packaged Power in this
repository were prepared as a transparent showcase layer.

The Kiro University submission window described by the owner closed on
5 October 2026. This repository was initialized after that deadline and must not
be represented as an on-time entry.

## Kiro artifacts

| Capability | Repository evidence | Activation evidence |
| --- | --- | --- |
| Spec-driven development | `.kiro/specs/grounded-answer-safety/` | Open the spec in Kiro and execute or review its tasks. |
| Steering | `.kiro/steering/` | Automatically loaded by Kiro from the workspace. |
| Hook | `.kiro/hooks/python-quality.json` | Save a Python file in Kiro and record the successful hook run. |
| Property-based testing | Requirements in the grounded-answer spec | Generate and run correctness properties in Kiro IDE; this has not been claimed merely by adding files. |
| Power | `kiro-power-dakikobo-safety/` | Import the folder as a custom Power and test an activation keyword. |
| MCP | `.kiro/settings/mcp.json` | Enable MCP, start the workspace server, and demonstrate a read-only repository query. |
| Custom agent | `.kiro/agents/agronomy-safety-reviewer.md` | Select the agent in Kiro and run a grounded-answer review. |

Configuration files are evidence of preparation. A form answer should claim
actual use only after the corresponding Kiro interaction has been performed and
shown in the demo video.

## Verification

The application remains governed by the commands in `AGENTS.md`. Kiro-specific
JSON can be checked with:

```bash
python -m json.tool .kiro/hooks/python-quality.json >/dev/null
python -m json.tool .kiro/settings/mcp.json >/dev/null
python -m json.tool kiro-power-dakikobo-safety/plugin.json >/dev/null
```
