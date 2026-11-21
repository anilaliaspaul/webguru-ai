<div align="center">
  <img src="skills/website-auditor.ai/assets/website-auditor-icon.svg" alt="website-auditor.ai icon" width="120">
  <h1>website-auditor.ai</h1>
  <p><strong>Inspect. Fix. Verify. Release with confidence.</strong></p>
  <p>An AI Agent Skill for comprehensive website quality assurance and authorized defect remediation.</p>
</div>

**website-auditor.ai** combines the work of a senior website QA manager, a senior full-stack developer, and an independent QA re-validation specialist.

It is packaged for Claude Code, ChatGPT Codex, and compatible Agent Skills hosts.

## Capabilities

| Mode | Responsibility | Deliverable |
|---|---|---|
| Audit Website | Inspect pages, journeys, and quality attributes | Evidence-based QA report and defect register |
| Fix QA Issues | Diagnose root causes and implement approved changes | Updated source code and implementation report |
| Re-Audit Website | Independently verify fixes and regression behaviour | QA validation and release recommendation |
| Full Cycle | Run the complete workflow with approval gates | Audit → Fix → Independent Re-Audit |

## 12 audit categories

1. Functional behaviour and user journeys
2. UI/UX and visual consistency
3. Responsive design
4. Cross-browser compatibility
5. Content and media
6. Accessibility — WCAG 2.2 AA
7. Performance and Core Web Vitals
8. Technical SEO
9. Security — OWASP-aligned
10. Third-party integrations
11. Technical and infrastructure readiness
12. UAT and go-live readiness

Findings use evidence, severity, priority, and explicit statuses. The skill does not invent test results or claim coverage of inaccessible systems.

## Installation

### Claude Code

Install globally:

```bash
npx skills add https://github.com/anilaliaspaul/webguru-ai --skill website-auditor.ai -a claude-code -g
```

Or copy `skills/website-auditor.ai` into your Claude Code skills directory.

### ChatGPT Codex

Copy `skills/website-auditor.ai` into your personal skills directory:

- macOS/Linux: `~/.agents/skills/website-auditor.ai`
- Windows: `%USERPROFILE%\.agents\skills\website-auditor.ai`

For project-level use, the repository includes `.agents/skills/website-auditor.ai/`.

## Invoke

- Claude Code: `/website-auditor.ai`
- Codex: `$website-auditor.ai`
- Compatible skill pickers: `@website-auditor.ai`, where supported.

On invocation, the skill asks which mode to run and gathers only the relevant inputs.

## Example prompts

**Website audit**

> Use website-auditor.ai to audit my staging website. Test the main user journeys, responsive layouts, accessibility, performance, SEO, and security. Produce a prioritized QA report with reproducible evidence.

**Fix reported defects**

> Use website-auditor.ai to inspect the attached QA report and fix the confirmed issues in my local repository. Work on a separate branch, run regression tests, and do not deploy.

**Independent re-audit**

> Use website-auditor.ai to re-test the original failed findings against the updated staging website and provide an independent release recommendation.

**Full cycle**

> Use website-auditor.ai to audit the website, show me the findings, wait for approval before changing source code, then fix and independently re-audit.

## Repository structure

```text
webguru-ai/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── ROADMAP.md
├── skills/
│   └── website-auditor.ai/
│       ├── SKILL.md
│       ├── agents/openai.yaml
│       └── assets/website-auditor-icon.svg
├── .claude/skills/website-auditor.ai/SKILL.md
└── .agents/skills/website-auditor.ai/SKILL.md
```

The repository name remains `webguru-ai`; the installed skill name and directory are now `website-auditor.ai`.

## Safety and limitations

- A website URL does not grant source-code, server, or production access.
- Source changes and deployments require explicit authorization.
- Security testing must stay within the agreed scope and avoid destructive activity.
- Browser-only inspection cannot prove private backend or infrastructure health.
- Automated accessibility and performance scans do not replace manual evaluation.
- Developer completion is not independent QA approval.

## Version

**1.0.0 — Initial release of website-auditor.ai**

## License

MIT. See [LICENSE](LICENSE).
