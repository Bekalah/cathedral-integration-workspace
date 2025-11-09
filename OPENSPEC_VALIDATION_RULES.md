# OpenSpec Validation Rules for Cathedral of Circuits
## Integration with Turbo and AI Assistant Protocols

## Core OpenSpec Principles

### 1. Session Start Protocol
**ALWAYS** begin by saying:
- "Read AI_AGENT_SELF_RULES.md first"
- "Read package.json and turbo.json before making changes"
- "Follow your OpenSpec protocols"
- "Show git diff to prove changes work"

### 2. Anti-Vibe Coding Protocol
- **NEVER** make assumptions about "standard" versions or configurations
- **ALWAYS** check actual files before suggesting changes
- **NEVER** hallucinate solutions - verify with file contents
- **ALWAYS** assume user has latest stable versions of all development tools
- **SAY "I DON'T KNOW"** instead of generating plausible but wrong answers

### 3. Validation and Proof Requirements
- **ALWAYS** show git diff as proof of changes
- **ALWAYS** run validation to confirm success before claiming "fixed"
- **NEVER** claim "I fixed it" without showing evidence
- **DEMONSTRATE** validation passes with concrete proof

### 4. Token Efficiency Protocol
- **BATCH** tool calls efficiently to avoid waste
- **STOP** when operations are cancelled
- **TRACK** token usage and avoid redundant calls
- **PRIORITIZE** essential operations over exploratory ones

## Turbo-Specific OpenSpec Rules

### Turbo Configuration Validation
```json
// ALWAYS verify turbo.json structure before changes
{
  "$schema": "https://turbo.build/schema.json",
  "ui": "tui",
  "tasks": {
    "build": {
      "outputs": ["dist/**", ".next/**", "!.next/cache/**"],
      "env": ["NODE_ENV", "CI", "TURBO_TOKEN", "TURBO_TEAM"]
    }
  },
  "globalDependencies": ["package.json", "turbo.json"],
  "globalEnv": ["NODE_ENV", "CI", "TURBO_TOKEN", "TURBO_TEAM"]
}
```

### Turbo Remote Caching Rules
- **CHECK** TURBO_TOKEN availability before enabling remote caching
- **MAKE** remote caching optional in CI/CD pipelines
- **VALIDATE** local caching works without remote access
- **DOCUMENT** when remote caching is disabled

### Turbo Build Validation
- **VERIFY** turbo.json syntax before running builds
- **CHECK** task dependencies are correctly defined
- **VALIDATE** output paths match actual build outputs
- **TEST** builds work locally before CI deployment

## AI Assistant Integration Rules

### File Reading Requirements
- **READ** AI_AGENT_SELF_RULES.md at session start
- **READ** package.json and turbo.json before any changes
- **READ** relevant configuration files before suggestions
- **VERIFY** actual file contents vs assumptions

### Proof of Work Requirements
- **SHOW** git diff for all changes made
- **DEMONSTRATE** validation passes
- **PROVE** builds complete successfully
- **EVIDENCE** deployments work correctly

### Scope Recognition Protocol
**NEVER** reduce Cathedral of Circuits to "sacred geometry" alone:
- **ALWAYS** acknowledge: Alchemy, Hermeticism, Kabbalah, Reiki, esoteric wisdom
- **INCLUDE**: Academic research, anthropology, physics, mathematics, architecture
- **RECOGNIZE**: Traditional and modern art, design, secret teachings
- **MAINTAIN**: "Unified Wisdom, Science, Art, and Design" mission scope

## GitHub Actions OpenSpec Rules

### CI/CD Pipeline Validation
- **MAKE** Turbo remote caching optional (TURBO_TOKEN conditional)
- **VALIDATE** workflows work with and without remote caching
- **CHECK** Node.js and pnpm versions match package.json
- **VERIFY** build artifacts are correctly uploaded

### Workflow Configuration Rules
```yaml
# ALWAYS make Turbo optional in CI
- name: Build
  run: pnpm build
  env:
    TURBO_TOKEN: ${{ secrets.TURBO_TOKEN }}
    TURBO_TEAM: ${{ vars.TURBO_TEAM }}
  if: env.TURBO_TOKEN != ''  # Make optional
```

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

## Cathedral of Circuits Scope Declaration

**This project encompasses:**
- **Alchemy, Hermeticism, Kabbalah, Reiki, esoteric wisdom**
- **Academic research, anthropology, physics, mathematics, architecture**
- **Traditional and modern art, design, secret teachings**
- **Unified Wisdom, Science, Art, and Design** - the complete mission

**NEVER** reduce this work to "sacred geometry" alone.
**ALWAYS** acknowledge the comprehensive scope and traditions.

---

*"In the sacred architecture of code, every validation builds the temple of truth."*