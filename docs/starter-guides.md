# What an open-source starter hands a team, and what stays the team's job

This repository, `Kortix-seo/open-source-claude-cowork-starter`, is a working Kortix project: one ops agent, one skill, a `kortix.yaml` that governs it, and a self-host path. The structure arrives on day one; the decisions about reach, review and hosting stay with the team.

## Skills and connectors are files

An agent is `agents/<name>.md` (behavior) plus an `agents.<name>` block in `kortix.yaml` (governance). A skill is a folder holding a `SKILL.md`, and a connector grant names the one connector an agent may call. The [plugins page](https://opensourceclaudecowork.com/claude-cowork-plugins) maps a plugin's four parts onto that layout and names what a fork cannot reach: the install, the network path the call takes, and the processes beside it.

Reach comes from a connector catalog. 3,000+ apps in a click, plus MCP, OpenAPI, Postman, GraphQL and raw HTTP. Connector credentials are brokered server-side and never enter the machine.

## Where the workspace runs

The [self-hosted workspace guide](https://opensourceclaudecowork.com/self-hosted-ai-workspace) separates the two layers a team buys separately: the tooling that turns a model into finished work, and the model. Kortix runs the first as one stack on a Linux server, with each session on a managed sandbox that calls back to the instance, so the server stays small and reachable. Run it on Kortix Cloud, in your VPC, or on your own on-prem network. Self-host is free.

The team still owns reach, approvals and merges. The repository's `docs/` covers the self-host steps, the comparison, and the questions to settle before installing.
