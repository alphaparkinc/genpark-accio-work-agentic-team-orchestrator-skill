---
name: accio-work-agentic-team-orchestrator
description: Distilled from Accio Work (accio.com). Provides execution-oriented multi-agent team orchestration, CDP browser control, and MCP server tooling.
version: 1.0.0
category: Service
author: GenPark AI Ecosystem
---

# Accio Work Agentic Team Orchestrator Skill

## Overview
This skill grants agents the capacity to coordinate multi-worker sub-teams under a Team Lead role, operate headless/headed browsers with DevTools Protocol, and schedule periodic automation tasks locally.

## Exposed Tools

### 1. `orchestrate_team_task`
- Description: Spawns specialized subagents (Researcher, Scribe, Operator) and directs their progress.
- Parameters: `goal` (string), `teamStructure` (object), `timeoutMs` (number).

### 2. `cdp_browser_action`
- Description: Performs controlled browser automation with snapshot auditing and selector clicking.
- Parameters: `action` (enum: click, type, screenshot, evaluate), `selector` (string), `url` (string).

### 3. `mcp_gateway_dispatch`
- Description: Relays external API queries through standardized Model Context Protocol tools.
