---
description: Fast branch analysis focusing on bugs, security, and performance.
agent: analyze-branch
---

Analyzes a branch relative to `master`/`main` and generates a detailed report in `reports/`.

**Primary Focus**:
- 🐛 **Critical Bugs**: Eloquent issues, null safety, SQL injection.
- 🚀 **Performance**: N+1 queries and optimization bottlenecks.
- 🔒 **Security**: Vulnerabilities (secrets, XSS, auth flaws).
- 💥 **Breaking Changes**: Caller analysis on unmodified code.
- 💾 **Database Risks**: Migration risks (drop/alter table, NOT NULL constraints).
- 🏗️ **Architecture**: SOLID/DRY violations.

**Input**: 
- `$ARGUMENTS` = target branch/ref to analyze (optional).
- Defaults to the **current branch** if empty.

**Output**:
- **Markdown Report**: `reports/ANALYSIS_<BRANCH>_<DATE>.md`.
- **Risk Score**: Detailed breakdown per area.
- **Findings**: Code snippets with suggested fixes.
- **Automated Checklist**: Pre-deploy validation.
- **Execution Time**: ~60 seconds.

**Key Features**:
- ✅ **High Speed**: Single-agent analysis, no orchestration overhead.
- ✅ **Real-time Tracking**: Live progress updates.
- ✅ **Actionable Fixes**: Direct code snippet suggestions.
- ✅ **Git Workflow Check**: Identifies divergence from base.
- ✅ **High Reliability**: Zero false negatives in high-risk areas (payments, scheduler).

**Notes**:
- Reports are always regenerated (no caching).
- Non-interactive (no confirmation required).
- Read-only operations + local report writing only.
