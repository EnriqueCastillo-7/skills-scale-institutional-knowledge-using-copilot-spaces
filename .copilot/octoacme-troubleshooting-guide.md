# OctoAcme Troubleshooting & FAQ Guide

Common issues and solutions for OctoAcme project management and Copilot Spaces usage.

## Project Management Issues

### Issue: Project is behind schedule

**Symptoms:**
- Velocity trending downward
- Tasks regularly slipping to next sprint
- Team reporting low capacity or blockers

**Diagnosis Questions:**
- Are dependencies blocking progress? (Escalate to Level 2)
- Is scope creeping during execution? (Return to Product Lead)
- Are team members context-switching? (Review resource allocation)
- Are tasks properly broken down into shippable increments?

**Solution Steps:**
1. Conduct standup with team to surface blockers
2. If blocking issues: escalate to PM → Product Lead → Sponsor
3. Review backlog prioritization with Product Lead
4. Consider breaking tasks into smaller, shippable pieces
5. Realign timeline with stakeholders if needed
6. Add action items to next retrospective

---

### Issue: Quality metrics declining

**Symptoms:**
- Increased bug reports
- Test failures in CI
- Security vulnerabilities found post-release
- Customer complaints about defects

**Root Causes:**
- Insufficient testing (skipped unit/integration tests)
- Not following PR review process
- Inadequate test coverage
- Security scanning gaps

**Solution Steps:**
1. Enforce CI quality gates (require passing tests before merge)
2. Increase code review rigor - check test coverage
3. Add missing test cases for newly discovered bugs
4. Run security scanner on all PRs
5. Add quality metrics to retrospective
6. Consider pair programming for high-risk areas

---

### Issue: Unclear decision-making or role confusion

**Symptoms:**
- Team unsure who decides on X
- Different team members making conflicting decisions
- Decisions being re-litigated repeatedly

**Solution Steps:**
1. Reference role definitions in `docs/octoacme-roles-and-personas.md`
2. Clarify escalation paths (Level 1 → 2 → 3)
3. Document decision in PR or issue comments
4. Add decision and rationale to retrospective notes
5. Update process docs if clarity needed for future teams

---

### Issue: Team morale or psychological safety concerns

**Symptoms:**
- Team reluctant to speak up in standups
- Avoiding retrospectives
- Reluctance to escalate blockers

**Solution Steps:**
1. Review OctoAcme principles: psychological safety is core
2. Ensure retrospectives are blameless (focus on systems, not people)
3. Encourage team to surface issues early
4. Create psychological safety by:
   - Acknowledging mistakes without blame
   - Celebrating learning from failures
   - Encouraging diverse perspectives
5. Consider 1-1 check-ins with team members
6. Raise with team lead or HR if patterns persist

---

## Copilot Spaces & Context Issues

### Issue: Copilot not giving context-aware responses

**Symptoms:**
- Copilot doesn't reference OctoAcme processes
- Suggestions don't align with team standards
- Copilot seems to lack knowledge of the docs

**Diagnosis:**
- Is the repository added as a source to your Copilot Space?
- Have you added `.copilot/` and `docs/` folders as sources?
- Has the repository been indexed? (Can take 30 seconds to a few minutes)
- Are you referencing the Space or using general Copilot?

**Solution Steps:**
1. Open your Copilot Space: https://github.com/copilot/spaces
2. Click on "OctoAcme Project Management Hub"
3. Verify repository appears in Sources
4. Check that `docs/` and `.copilot/` folders are included
5. Wait 30-60 seconds for indexing if just added
6. Try a new question referencing the processes
7. If still not working, try removing and re-adding the repository

---

### Issue: Copilot giving multiple contradictory suggestions

**Symptoms:**
- In a single response, Copilot suggests different approaches
- Suggestions conflict with documented processes

**Why This Happens:**
- Copilot may be drawing from general knowledge vs. specific context
- Repository context may not have been fully indexed yet
- Question might be ambiguous

**Solution:**
1. Be specific in your prompt: "Based on OctoAcme process docs..."
2. Reference specific files: "According to docs/octoacme-execution-and-tracking.md..."
3. Rephrase if answer is unclear
4. Re-index sources in your Space if needed

---

### Issue: Cannot find my Copilot Space

**Symptoms:**
- Space disappeared or can't locate it
- Created a Space but it's not showing in "Yours"

**Solution:**
1. Go to https://github.com/copilot/spaces
2. Click **"Yours"** tab to see your personal Spaces
3. Look for "OctoAcme Project Management Hub"
4. If not there, create a new Space with that exact name
5. Add repository as source again

---

## GitHub & Repository Issues

### Issue: Cannot create pull requests or merge fails

**Symptoms:**
- "Permission denied" error
- PR merge blocked
- Cannot push to branch

**Check:**
1. Do you have push access to this repository?
2. Are you working on a protected branch? (should branch from `main`)
3. Do all required checks pass? (CI, tests, etc.)
4. Is the PR approved? (require 1 approval)

**Solution:**
1. Verify you have Collaborator or higher permission
2. Always create branches from latest `main`
3. Ensure all CI checks pass before requesting review
4. Get approval from another team member
5. Contact repo owner if permission issue

---

### Issue: Merge conflicts when pulling latest main

**Symptoms:**
- "CONFLICT: merge conflict" error
- Cannot complete merge

**Solution:**
1. Fetch latest `main`: `git fetch origin main`
2. Rebase your branch: `git rebase origin/main`
3. Resolve conflicts (edit conflicted files)
4. Add resolved files: `git add .`
5. Complete rebase: `git rebase --continue`
6. Force push your branch: `git push origin [branch-name] --force`
7. Retry PR merge

---

## General FAQ

**Q: How often should we run retrospectives?**
A: After each sprint (typically 2 weeks), each release, or after significant incidents. Minimum: monthly.

**Q: What's the expected velocity?**
A: Velocity should be tracked per team and sprint. It varies based on team size, complexity, and process maturity. Focus on consistency and trends rather than absolute numbers.

**Q: Can we change the process?**
A: Yes! OctoAcme processes are living documents. Propose changes via issues using the "Add Content to Project Management Process Docs" template. Discuss in retrospectives and update docs accordingly.

**Q: How do we handle emergency/hotfix situations?**
A: Use the hotfix process: shorter planning cycle, expedited review (2+ approvals recommended), immediate release to production, and post-incident retrospective.

**Q: What if a decision contradicts documented process?**
A: Document the decision, decision date, decision-maker, and rationale in a comment or issue. Then update the process docs if the change should be permanent.

---

**Still stuck?** Ask in your team Slack or reference the main documentation in `docs/`.
