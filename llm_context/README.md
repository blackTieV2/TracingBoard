# Tracing Board TB-1 LLM Context Pack

Purpose: provide structured, LLM-first source-of-truth files for the next phase of the Tracing Board rebuild.

This pack intentionally avoids long policy essays. The primary context is YAML so that Codex, Lovable, ChatGPT, and future agents can parse and act on it consistently.

Recommended repo destination:

- `llm_context/`
- `00_project_control/status/PHASE-TB1-STATUS.yaml`

Primary rule:

Agents must treat these YAML files as instruction/context inputs, not as decorative documentation.

Suggested next workflow:

1. Add this pack to the `TracingBoard` repo.
2. Commit it on a feature branch.
3. Ask Codex to review the YAML for consistency and create a pull request.
4. Use `llm_context/lovable_build_brief.yaml` as the input brief for Lovable.
5. Use `llm_context/codex_handoff.yaml` as the operational prompt for Codex.
