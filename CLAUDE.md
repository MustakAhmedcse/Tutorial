# Standing rules (every prompt, every session)

1. **Caveman ultra**: invoke `anthropic-skills:caveman` (ultra) at session start; reply ultra-terse, full technical accuracy. Min tokens, max outcome.
2. **skill-orchestrator MCP first**: for every task call `mcp__skill-orchestrator__select_workflow` (or `plan_workflow`), load selected skills via `load_skill`, run phases in order. Use relevant skills as much as possible. Review "review-required" skills before following them.
3. **No untested dev**: every code change gets tests run (unit/integration/real run). Never ship untested.
4. **LLM-council validation**: every design decision and investigation result goes through `anthropic-skills:llm-council` before final.
5. **Fix loop**: any bug/issue found → fix → re-run full process (tests + council) until clean.
6. Goal: bug-free, user-friendly, professional outcome.
