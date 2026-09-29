# Agent bootstrap: start at the Council

This file is a bootstrap, not documentation. It holds the address of the contract, not the contract, and it loses every conflict with the cortex: where the two disagree, the cortex is right and this file is stale.

## Ground in this order

1. `cortex.ground` on instance `100monkeys-ai`; its payload lists every workspace with its UUID. Name the `council` workspace by that UUID and read the Council `home`, then `roster`.
2. No workspace governs this repository and no seat on the roster covers it (roster as of 2026-09-29). Your brief is the contract; raise what it does not settle with whoever spawned you.
3. Read the brief you were handed, by your project manager where the roster names one.

## Every cortex call names its workspace

"Pass your task's workspace as `workspace` on every call from here on; never call `me.set_current_workspace`, whose pointer every session on the token shares." The UUIDs come from `cortex.ground`; this file carries none.

## Where the contract lives

In the workspace grounding `cortex.ground` returns, and in the pages the roster names for this repository's seat, where it has one: contract, ledger, directives, rulings. Nothing here restates them.

`CLAUDE.md` is a symlink to this file, `AGENTS.md`; edit only this file.
