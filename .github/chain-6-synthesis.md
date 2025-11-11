---
model: gpt-4.1
---

# Step 6: Build Instructions (Synthesis)

Synthesize all previous chain steps into a comprehensive GitHub Copilot instructions file.

## Instructions

This final step combines outputs from:
1. Tech Stack (chain-1)
2. File Categorization (chain-2)
3. Architecture (chain-3)
4. Domain Deep Dive (chain-4)
5. Style Guides (chain-5)

Create a single, unified `.github/copilot-instructions.md` file that contains:

## Synthesis Structure

### 1. Repository Overview
- Project purpose (from README analysis)
- Tech stack summary (from chain-1)
- Target audience and use cases

### 2. Architecture Context
- High-level architecture (from chain-3)
- Component relationships
- Key integration points
- Data flows

### 3. File Organization
- Directory structure (from chain-2)
- File categorization patterns
- Naming conventions
- Where to find what

### 4. Domain Knowledge

For each key domain (from chain-4):
- Core concepts
- Implementation patterns in this repo
- Rules and constraints
- Code examples

### 5. Code Style & Conventions

For each file type (from chain-5):
- Mandatory patterns
- Preferred approaches
- Anti-patterns to avoid
- Real examples from the codebase

### 6. Development Guidelines

**When generating new code**:
- Follow established naming conventions
- Use existing patterns for similar functionality
- Maintain architectural consistency
- Apply domain-specific rules
- Match the style of surrounding code

**When modifying existing code**:
- Preserve existing patterns
- Maintain test coverage
- Update documentation
- Follow versioning practices

**When answering questions**:
- Reference actual code examples
- Consider healthcare/FHIR context
- Point to relevant samples
- Include compliance considerations

### 7. Project-Specific Rules

**Security**:
- No PHI in logs
- Use managed identities
- Secrets in Key Vault
- HTTPS/TLS for all communication

**Healthcare Standards**:
- FHIR R4/R5 compliance
- US Core profiles
- SMART on FHIR v2
- ONC (g)(10) requirements

**Testing**:
- xUnit + NSubstitute
- Given-When-Then naming
- AAA pattern
- MIT license header

**Infrastructure**:
- Bicep over ARM templates
- Azure Developer CLI
- Environment parameterization
- Resource tagging

### 8. Integration Guide

**Adding New Features**:
1. Review similar existing implementations
2. Follow domain patterns
3. Maintain architectural consistency
4. Add tests following conventions
5. Update documentation

**Working with Azure Services**:
- Authentication patterns
- Service interaction patterns
- Error handling and retry logic
- Logging and monitoring

**Working with FHIR**:
- Resource validation
- Search parameter handling
- Bundle processing
- Version compatibility

## Output Format

Create the final `copilot-instructions.md` file with:

```markdown
# GitHub Copilot Instructions

[Synthesized content from all 5 previous chain steps]

## Repository Context
[From chain-1 and README]

## Architecture
[From chain-3]

## Code Organization
[From chain-2]

## Domain Knowledge

### SMART on FHIR
[From chain-4]

### FHIR Resources
[From chain-4]

[etc...]

## Style Guides

### C# Files
[From chain-5]

### Test Files
[From chain-5]

[etc...]

## Development Rules
[Synthesized from all chains]

## Examples
[Real code examples from chain-4 and chain-5]
```

The final output should be a comprehensive, project-specific instruction file that enables GitHub Copilot to generate code that perfectly matches this repository's patterns, architecture, and conventions.
