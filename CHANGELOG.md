# Changelog

All notable changes to the Eesier Claude Code plugin will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-05-20

### Added

- Initial release of the Eesier plugin for Claude Code.
- MCP server registration pointing to `https://mcp.eesier.com` (reads `EESIER_MCP_TOKEN` env var).
- 49 MCP tools exposed to the agent across 8 areas: session, business profile, prospecting configuration, AI generation, campaigns, leads, reference data, Calendly integration, and reports.
- Bundled operator skill (`skills/eesier/SKILL.md`) with onboarding flow, tool reference, multi-business prospecting rules, lead operations, capability boundaries, settings inheritance, and safety/compliance guidance.
- Marketplace manifest enabling install via `/plugin marketplace add soviero/claude-plugins` + `/plugin install eesier@eesier`.
