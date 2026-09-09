# Boomi Custom Skills & AI Agent Tools

A centralized collection of enterprise **Dell Boomi** companion skills, static analysis engines, and architectural peer-review tools. 

Designed for seamless cross-compatibility with **Antigravity**, **Claude (Claude Code)**, **Cursor**, **Codex / GitHub Copilot**, and **Standalone CLI**.

---

## 📦 Available Skills Catalog

| Skill Name | Directory | Description | Trigger |
|---|---|---|---|
| **Boomi Code Review** | [`skills/boomi-code-review`](./skills/boomi-code-review) | Automated static analysis and architectural peer reviews enforcing Psiog Integrations standards, DB service user conventions (`SRV_`), Try/Catch resilience, batch halt dynamics, and sensitive credential protection. | `/boomi-code-review` <br> `@boomi-code-review` |
| *(Future Skills)* | `skills/<skill-name>` | Add your custom deployment, testing, or migration skills here. | — |

---

## 🛠️ Multi-Platform Compatibility

Every skill in this repository includes native adapters for major AI-assisted engineering environments:

| Platform / IDE | Discovery Location | Trigger Mechanism |
|---|---|---|
| **Antigravity / Gemini** | `.agents/skills/` | `/boomi-code-review [path]` |
| **Claude (Claude Code CLI)** | `.claude/commands/` or `CLAUDE.md` | `/boomi-code-review [path]` |
| **Cursor IDE** | `.cursor/rules/` | `@boomi-code-review` in Composer or auto-triggered on XML files |
| **GitHub Copilot / Codex** | `.github/copilot-instructions.md` | `@workspace /review` in Copilot Chat |
| **Standalone Terminal** | `skills/<skill>/scripts/` | `python skills/boomi-code-review/scripts/boomi_code_review.py <path>` |

---

## 🚀 Installation Guide for Peers

Choose how you want to install this collection:

### Option 1: Global Installation (Recommended)
Make **all** skills in this repository available across **every project** you open on your machine without needing to clone it into each project:

* **Windows (PowerShell):**
  ```powershell
  git clone https://github.com/<your-org>/boomi-custom-skills.git "$HOME\.gemini\boomi-custom-skills"
