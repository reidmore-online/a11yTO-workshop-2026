---
name: a11y-triage
description: Assess and prioritize accessibility issues from audit reports, then create a clear remediation plan. Use this skill when you have accessibility findings to sort out—whether from audits, user testing, or automated scans—and need to decide which issues to fix first. Prioritizes by impact on users and feasibility of fixes. Also use whenever someone asks to "triage accessibility issues", "prioritize A11y findings", "create an accessibility roadmap", or "organize A11y work".
---

# Accessibility Triage 

This skill takes accessibility issues from audit reports and helps you decide:
- **Which issues matter most** (priority ranking based on user impact)
- **What to fix first** (considering both importance and feasibility)
- **How to organize the work** (a clear roadmap for remediation)

It follows your team's accessibility policies and guidelines to ensure recommendations fit your context. 

## How It Works

This skill follows a simple three-step process:

### Step 1: Review what you have
Start with the issues you have. Ideally, each issue includes:
- **What's broken** (a brief summary)
- **Where/how to see it** (steps to reproduce)
- **What should happen instead** (expected behavior)
- **Which WCAG guideline is affected** (if known)
- **Screenshots or examples** (helpful but not required)

If some details are missing, that's OK—note what's unclear and keep going. Missing information might affect the priority assessment, but don't let perfect be the enemy of good.

### Step 2: Assess priority
For each issue, determine how urgent it is based on:
- **User impact**: Does this block someone from using the product, or is it a minor annoyance?
- **Scope**: How many users are affected?
- **Severity**: Can the user work around it, or are they stuck?

Use your team's priority framework (in [priority-scheme.md](references/priority-scheme.md)) as a guide.

### Step 3: Create a roadmap
Organize issues into a plan that balances:
- **Impact first**: Address high-impact issues before low-impact ones
- **Feasibility**: Consider which fixes are quick wins vs. require more work
- **Platform realities**: Account for tech-specific constraints (see [platform-considerations.md](references/platform-considerations.md))

The result is a clear remediation plan your team can act on.

## Reference Materials

These documents guide the triage process and should be tailored to your team's context:

- **[priority-scheme.md](references/priority-scheme.md)** — How to categorize issue severity and urgency (e.g., "Critical" vs. "Minor")
- **[accessibility-policies.md](references/accessibility-policies.md)** — Your team's standards and what you're committed to supporting
- **[platform-considerations.md](references/platform-considerations.md)** — Tech-specific constraints (e.g., which libraries, browsers, or assistive tech matter for your product)

## Output: Triage Report

This report lists all issues with their assigned priority. It's a snapshot of the assessment and helps your team see what you're working with.

**Format:**

The triage report must be formatted as a table as follows.

```markdown
# Accessibility Triage Report

Issues Reviewed: {number}
Date: {date}

| Summary | Description | WCAG/EN 301 549 Criteria | Priority |
|---------|-------------|---------------------------|----------|
| {summary} | {description} | {criteria} | {priority} |
```

**Example:**

| Summary | Description | WCAG/EN 301 549 Criteria | Priority |
|---------|-------------|---------------------------|----------|
| Button label missing | Search button has no visible text, only an icon | WCAG 2.1 1.1.1 (Text Alternatives) | High |
| Color contrast too low | Text on blue background fails contrast ratio | WCAG 2.1 1.4.3 (Contrast) | High |
| Form error unclear | Error message appears but not linked to field | WCAG 2.1 3.3.1 (Error Identification) | Medium |

The triage report should be saved in the `/bug-reports` folder with the file name `triage-report-{date}.md`.

## Output: Remediation Plan

This is your roadmap. It organizes issues by impact and feasibility, so your team knows where to focus effort and what makes sense to tackle together.

**Format:**

```markdown
# Accessibility Remediation Plan

Issues Reviewed: {number}
Date: {date}

## Summary
{Brief overview: how many issues, key themes, recommended approach}

## Phase 1: High Impact, Quick Wins
{High priority issues that are relatively easy to fix}

## Phase 2: High Impact, Moderate Effort
{High priority issues that need more work}

## Phase 3: Medium Impact or Lower Priority
{Lower priority fixes that can wait or be batched}
```

**What goes in each phase:**
- **Phase 1** helps you build momentum and show progress early
- **Phase 2** tackles the most important remaining work
- **Phase 3** captures debt you can address later or combine with other work

You can also organize by component, feature, or team if that fits your workflow better—adapt as needed.

The remediation plan should be saved in the `/bug-reports` folder with the file name `remediation-plan-{date}.md`.

## Tips for Success

- **Start with what you have.** Don't wait for perfect issue reports. Incomplete information is fine—note it in your assessment and move forward.
- **Lean on your guides.** Your priority-scheme and accessibility policies are there to make decisions easier. Reference them, but don't let them override your judgment about your actual users.
- **Think about phases.** A good remediation plan is one your team can execute. If everything is "critical," nothing is. Use phases to show progress and build momentum.
- **Revisit periodically.** Priorities change as you ship fixes and learn more. Retriage every quarter or when context shifts.