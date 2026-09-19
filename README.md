# GenPark Skill: Accio Work Agentic Team Orchestrator

[![GenPark Certified](https://img.shields.io/badge/GenPark-Certified%20Skill-00E599?style=flat-square)](https://genpark.ai)
[![Protocol](https://img.shields.io/badge/MCP-Model%20Context%20Protocol-6A0DAD?style=flat-square)](https://modelcontextprotocol.io)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=flat-square)](LICENSE)

> Distilled from [Accio Work](https://www.accio.com) - The autonomous business team architecture designed for execution-oriented agent collaboration, CDP browser automation, and local-first execution.

---

## 🌟 Core Architecture & Distilled Features

### 1. Multi-Agent Team Orchestration (Teams Pattern)
- **Team Lead (TL)**: Ingests macro business goals, decomposes them into structured sub-DAGs, and assigns tasks across specialized worker agents.
- **Role Specialization**: Market Researcher, SEO Copywriter, Financial Auditor, and Browser Scraper.
- **Dynamic Collaboration**: Workers communicate and hand off intermediate artifacts via structured internal channels.

### 2. CDP-Powered Autonomous Browser Engine
- Full Chrome DevTools Protocol integration with explicit permission gates.
- Automated navigation, form entry, anti-bot evasion, page scraping, screenshot recording, and receipt extraction.

### 3. Unified Model Gateway & Router
- Native routing support across Gemini 2.5 / 3.0, Claude 3.7 / 4.6 Sonnet, GPT-4o, and Qwen 2.5.
- Cost-aware task allocation: light verification to compact models, deep architectural reasoning to frontier models.

### 4. Open Model Context Protocol (MCP) Server
- Turn-key MCP tool server exposing local file execution, CLI terminal runner, and multi-channel notification bots (Slack, Discord, Telegram, DingTalk, Lark).

---

## 🚀 Quick Start

```bash
npm install @alphapark/accio-work-orchestrator-skill
```

```typescript
import { AccioTeamOrchestrator } from '@alphapark/accio-work-orchestrator-skill';

const team = new AccioTeamOrchestrator({
  mode: 'local-first',
  browserPermission: 'prompt-once',
  modelGateway: {
    defaultLead: 'claude-3-7-sonnet',
    defaultWorker: 'gemini-2.5-flash'
  }
});

// Launch an autonomous marketing & sourcing workflow
const result = await team.executeBusinessGoal({
  goal: "Perform competitive pricing distillation on trending AI hardware and prepare product cards",
  channels: ["discord-alerts"]
});

console.log("Team execution finalized:", result.summary);
```

---

## 📦 License
Apache-2.0 © 2026 GenPark AI Inc.
