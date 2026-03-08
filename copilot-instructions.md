# AEGIS Copilot Instructions

## Start Here

**Before working on any AEGIS component, read `aegis-architecture/AGENTS.md`.**

It is the canonical source for:
- Ubiquitous language (use these terms exactly — e.g., `Agent` not `Bot`, `Manifest` not `Config`, `Execution` not `Run`)
- All **14 bounded contexts** and their owners
- DDD layering rules (domain -> application -> infrastructure -> presentation)
- Anti-patterns to avoid

## Pre-Alpha Rule

**Do NOT add backward compatibility layers or preserve legacy code.** If you find any, remove them. Do NOT create new database migrations — update existing migrations (notably `aegis-orchestrator/cli/migrations/001_initial.sql`).
