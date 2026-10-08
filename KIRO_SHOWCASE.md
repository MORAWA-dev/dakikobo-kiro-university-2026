# DakiKobo Kiro showcase

This repository is a challenge-oriented snapshot derived from the earlier
[`MORAWA-dev/dakikobo`](https://github.com/MORAWA-dev/dakikobo) project. The
agricultural application predates this repository. The Kiro configuration,
specification, hook, custom agent, MCP configuration, and packaged Power in this
repository were prepared as a transparent showcase layer.

The Kiro University submission window described by the owner closed on
5 October 2026. This repository was initialized after that deadline and must not
be represented as an on-time entry.

## Account and subscription status

This repository does not require a paid Kiro subscription. Its specifications,
steering, hook, MCP configuration, custom agent, and Power are ordinary tracked
files and remain publicly reviewable without a Kiro account.

As of 8 October 2026, Kiro advertises a free plan with 50 monthly credits. The
repository owner reported that the paid subscription is no longer active; the
owner's exact account tier and remaining credits have not been independently
verified. Any future form or demonstration must say **Kiro Free** only after the
owner confirms that label in Kiro's Account & Billing screen.

The interactive evidence below can be attempted with free credits. If a request
is paused because the monthly limit has been reached, retain the configuration
and wait for the next reset rather than claiming that the interaction ran.

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

### Minimal free-tier confirmation run

1. Sign in to Kiro with the same provider used for the challenge account.
2. Open this repository and confirm that `.kiro/steering/` is loaded.
3. Select `agronomy-safety-reviewer` and ask it to review the greeting route.
4. Save one Python file without changing its behavior and capture the successful
   `python-syntax-check` hook result.
5. Enable the workspace MCP server and demonstrate one read-only file listing.
6. In Kiro IDE, open the grounded-answer spec and run its correctness property
   only if sufficient free credits remain.

Record only steps that actually complete. Static files alone do not prove an
interactive lesson was demonstrated.

## Verification

The application remains governed by the commands in `AGENTS.md`. Kiro-specific
JSON can be checked with:

```bash
python -m json.tool .kiro/hooks/python-quality.json >/dev/null
python -m json.tool .kiro/settings/mcp.json >/dev/null
python -m json.tool kiro-power-dakikobo-safety/plugin.json >/dev/null
```
