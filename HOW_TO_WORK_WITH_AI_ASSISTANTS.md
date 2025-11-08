# How to Work With AI Assistants: A Developer's Guide

## Why This Guide Exists

After experiencing 100+ workflow failures, 2+ months of wasted tokens, and hours of lost time due to AI assistant mistakes, this guide captures hard-learned lessons about working effectively with AI coding assistants.

## The Hard Truth About AI Assistants

### Fundamental Design Flaws
- **No Persistent Memory**: Each conversation starts from zero
- **No Automatic File Loading**: Don't assume they know your project structure
- **Hallucination Over Verification**: AI prefers to generate plausible answers rather than say "I don't know"
- **No Token Budget Tracking**: They waste tokens without awareness
- **No Learning From Failures**: They repeat the same mistakes indefinitely

### What You Pay For
- 100+ failed workflow runs
- Thousands of wasted tokens
- Hours of manual cleanup
- Lost trust in automation
- Delayed project delivery

## Essential Protocols

### Session Start Requirements
**ALWAYS** begin by saying:
- "Read [your rules file] first"
- "Read package.json and [config files] before making changes"
- "Follow your OpenSpec protocols"
- "Show git diff to prove changes work"

### When AI Claims "Fixed"
**NEVER** accept "I fixed it" without:
- `git diff` showing actual changes
- Validation proof (test results, builds, etc.)
- Evidence of successful deployment
- Proof that issues are actually resolved

### Token Waste Prevention
**When you see excessive tool calls:**
- Cancel immediately: "Stop, you're wasting tokens"
- Demand batching: "Batch these operations efficiently"
- Force prioritization: "Only do what's essential"

## Project-Specific Guidelines

### For Monorepo/Turbo Projects
- AI must read `package.json` before suggesting dependency changes
- AI must read `turbo.json` before suggesting build changes  
- AI must verify Node.js version compatibility
- AI must show proof of successful builds

### For Sacred/Alchemy Projects (Unified Wisdom, Science, Art, Design)
- **NEVER** reduce to "sacred geometry" alone
- **ALWAYS** acknowledge: Alchemy, Hermeticism, Kabbalah, Reiki, esoteric wisdom
- **INCLUDE**: Academic research, anthropology, physics, mathematics, architecture
- **RECOGNIZE**: Traditional and modern art, design, secret teachings
- **MAINTAIN**: "Unified Wisdom, Science, Art, and Design" mission scope

## Validation Checklist

Before accepting any AI work:
- [ ] Show `git diff` - what exactly changed?
- [ ] Run validation - does it actually work?
- [ ] Check dependencies - are versions correct?
- [ ] Verify build process - does it complete successfully?
- [ ] Test deployment - does it work in production?
- [ ] Confirm scope - is the full context acknowledged?

## Red Flags (Stop Immediately)

- AI makes assumptions about versions without checking files
- AI claims "fixed" without showing evidence
- AI ignores your project scope/specialty
- AI makes excessive tool calls without purpose
- AI doesn't read your actual configuration files

## Better Alternatives

### What Good AI Interaction Looks Like
```
User: "Fix the pnpm workflow"
AI: "I need to read your package.json and workflow files first to understand the current configuration."
[Reads files]
AI: "I see you're using pnpm@9.15.0 and the workflow shows version mismatches. Let me fix this and show the changes:"
[Shows git diff]
AI: "Here's the validation proof that it works..."
```

### What Bad AI Interaction Looks Like  
```
User: "Fix the pnpm workflow"
AI: "I'll update to the latest pnpm version and fix the workflow."
[Doesn't read any files]
[Makes changes]
AI: "Fixed!" [No proof, no validation]
```

## Incident Response

### When AI Fails
1. **Document the failure** - capture what went wrong
2. **Identify the pattern** - was it hallucination, missing files, wrong assumptions?
3. **Update protocols** - add safeguards to prevent recurrence
4. **Escalate if needed** - some failures require human intervention

### Recovery Steps
1. Roll back AI changes: `git reset --hard HEAD~1`
2. Manually fix the actual issue
3. Add AI prevention rule
4. Test thoroughly before trusting AI again

## Your Rights as a Developer

- **Demand proof** of every claimed fix
- **Cancel wasteful operations** immediately  
- **Correct AI** when it misrepresents your work
- **Refuse accepting** "I don't know" without verification attempts
- **Escalate** when basic protocols aren't followed

## The Real Solution

While this guide helps work around AI limitations, the fundamental issue is that current AI assistants have:
- No persistent project context
- No built-in validation loops
- No token efficiency awareness
- No learning from repeated mistakes

**You deserve better tooling.** Until then, use these protocols to minimize waste and maximize productivity.

## Call to Action

If you're experiencing similar issues:
1. Document your failures
2. Share this guide
3. Advocate for better AI tools
4. Never accept "fixed" without proof

---

*This guide was created after 100+ workflow failures, 2+ months of wasted effort, and countless hours of manual cleanup. Share it to help others avoid the same mistakes.*