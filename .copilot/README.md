# Copilot Context Configuration

This folder contains curated content to ground GitHub Copilot's knowledge in OctoAcme's project management processes and institutional knowledge.

## Purpose

The files in this directory are designed to:
- Provide Copilot with comprehensive context about OctoAcme's project management approach
- Enable context-aware code and documentation suggestions
- Ensure consistent guidance aligned with OctoAcme's processes and best practices
- Support team members in writing code that follows established patterns and procedures

## How It Works

When you use GitHub Copilot Spaces with this repository:
1. Copilot indexes the files in this folder (`.copilot/`)
2. These files provide structured context for AI suggestions
3. Copilot references this knowledge when responding to questions and generating code
4. Results are more aligned with OctoAcme's standards and practices

## Contents

- **octoacme-process-index.md** — Quick reference index of all key processes
- **octoacme-coding-standards.md** — Development standards and best practices
- **octoacme-review-checklist.md** — Code review guidelines and quality gates
- **octoacme-troubleshooting-guide.md** — Common issues and solutions

## Adding More Context

To add new context files:
1. Create a new `.md` file in this directory
2. Use the naming convention: `octoacme-[topic].md`
3. Include clear headers and examples
4. Reference the main process docs when relevant
5. Submit a PR with the new file and update this README

## Integration with Copilot Spaces

This context is automatically picked up by Copilot Spaces when:
- The repository is added as a source to a Copilot Space
- You reference files from this folder in your Space
- You use prompts that request context-aware assistance

For more information about Copilot Spaces, see the [main README](../README.md).
