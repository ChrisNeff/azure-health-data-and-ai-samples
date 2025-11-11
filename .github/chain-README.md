# GitHub Copilot Prompt Chaining Guide

## Overview

This directory contains a **prompt chain** - a curated sequence of six steps designed to give GitHub Copilot deep contextual understanding of this codebase. Instead of generic code generation, Copilot will act like an experienced team member who knows the project's architecture, conventions, and patterns.

## What is Prompt Chaining?

Prompt chaining builds context piece by piece, with each step building on the previous ones. The result is a comprehensive Copilot instructions file that contains all necessary rules, style guides, and integration points specific to this repository.

### The Six-Step Chain

1. **chain-1-tech-stack.md** - Identify languages, frameworks, and libraries
2. **chain-2-categorize-files.md** - Organize files by purpose and type
3. **chain-3-architecture.md** - Map how components fit together
4. **chain-4-domain-deep-dive.md** - Document domains with real code examples
5. **chain-5-style-guides.md** - Extract unique conventions for each file type
6. **chain-6-synthesis.md** - Synthesize everything into final instructions

## Why Use Prompt Chaining?

**Without context**, GitHub Copilot generates generic code that may not match your:
- Naming conventions
- Architectural patterns
- Domain-specific requirements
- Testing standards
- Security practices

**With prompt chaining**, Copilot learns your codebase and generates code that:
- Matches existing patterns perfectly
- Follows established conventions
- Integrates properly with architecture
- Respects domain rules
- Uses the right libraries and approaches

## How to Use This Prompt Chain

### Method 1: Sequential Execution (Recommended for First Time)

Execute each step in order, saving outputs:

#### Step 1: Tech Stack Analysis

1. Open GitHub Copilot Chat
2. Reference the first prompt: `@workspace /chain-1-tech-stack.md`
3. Let Copilot analyze the repository
4. **Save the output** to a temporary file or note

**Output**: List of all technologies, frameworks, and tools used

#### Step 2: File Categorization

1. In Copilot Chat: `@workspace /chain-2-categorize-files.md`
2. Copilot will scan and categorize all files
3. **Save the output** showing file organization patterns

**Output**: Hierarchical categorization of files by purpose

#### Step 3: Architecture Mapping

1. In Copilot Chat: `@workspace /chain-3-architecture.md`
2. Copilot maps component interactions
3. **Save the output** documenting the architecture

**Output**: Component relationships, data flows, integration points

#### Step 4: Domain Deep Dive

1. In Copilot Chat: `@workspace /chain-4-domain-deep-dive.md`
2. Copilot extracts domain knowledge with real examples
3. **Save the output** showing domain patterns

**Output**: Domain concepts, code examples, patterns, and rules

#### Step 5: Style Guide Extraction

1. In Copilot Chat: `@workspace /chain-5-style-guides.md`
2. Copilot analyzes code to extract conventions
3. **Save the output** documenting style patterns

**Output**: File-type-specific conventions with real examples

#### Step 6: Synthesis

1. In Copilot Chat: `@workspace /chain-6-synthesis.md`
2. Provide Copilot with **all previous outputs**
3. Copilot synthesizes into final instructions
4. **Save to** `.github/copilot-instructions.md`

**Output**: Comprehensive Copilot instructions file

### Method 2: Single Magic Prompt (Advanced)

After running the chain once, you can create a single prompt that executes all steps:

```markdown
@workspace Execute the Bitovi prompt chain:

1. Analyze tech stack (chain-1)
2. Categorize all files (chain-2)
3. Map architecture (chain-3)
4. Document domains with examples (chain-4)
5. Extract style guides (chain-5)
6. Synthesize all results into final copilot-instructions.md (chain-6)

For each step, build upon the previous step's output.
Generate the final comprehensive instructions file.
```

This produces the final instructions file in one execution, but requires more tokens and may need refinement.

## Practical Workflow

### Initial Setup (First Time)

1. **Run the sequential chain** (Method 1) to understand what each step produces
2. **Review each output** to ensure accuracy
3. **Refine prompts** if needed for your specific repository
4. **Generate final** `copilot-instructions.md`
5. **Test with Copilot** by asking it to generate code

### Maintenance (Updates)

When your codebase evolves significantly:

1. **Re-run relevant chains**:
   - New tech? Re-run chain-1
   - New file types? Re-run chain-2
   - Architecture change? Re-run chain-3
   - New domain patterns? Re-run chain-4
   - Convention changes? Re-run chain-5

2. **Re-synthesize** with chain-6 using updated outputs

3. **Update** `copilot-instructions.md`

## Tips for Best Results

### 1. Be Specific
When running chains, provide specific examples or focus areas if Copilot's output is too generic.

### 2. Review and Refine
Each chain output should be reviewed. If something doesn't match your codebase, refine the prompt or provide corrections.

### 3. Use Real Examples
Chain-4 and chain-5 work best when Copilot pulls actual code from your repository. Encourage it to reference specific files.

### 4. Iterate
The first run might not be perfect. Run chains again with refined prompts based on initial results.

### 5. Keep Updated
As your codebase evolves, periodically re-run the chain to keep Copilot's understanding current.

## What to Do with the Results

### The Final Instructions File

Once you have `copilot-instructions.md`:

1. **Place it** in `.github/copilot-instructions.md`
2. **GitHub Copilot automatically reads it** when suggesting code
3. **Test it** by asking Copilot to:
   - Generate a new function
   - Create a test
   - Write infrastructure code
   - Explain architecture

### Verify It's Working

Ask Copilot questions like:
- "Generate a new Azure Function following project conventions"
- "Create a unit test for XYZ class"
- "How should I integrate a new FHIR resource handler?"

If Copilot references your specific patterns, conventions, and architecture, the chain was successful!

## Example Usage Scenarios

### Scenario 1: New Developer Onboarding

```markdown
@workspace Using the copilot instructions, explain:
1. The overall architecture
2. How to add a new SMART on FHIR operation
3. Testing conventions I must follow
4. Where to find examples of similar code
```

### Scenario 2: Generating New Code

```markdown
@workspace Create a new Azure Function that validates FHIR Patient resources.
Follow all project conventions for:
- File structure
- Naming
- Error handling
- Logging
- Testing
```

### Scenario 3: Refactoring

```markdown
@workspace Refactor this code to match our established patterns:
[paste code]

Ensure it follows:
- Our architectural patterns
- Domain-specific rules
- Style guide conventions
```

## Chain Files Reference

| File | Purpose | Output |
|------|---------|--------|
| `chain-1-tech-stack.md` | Discover technologies | Tech stack inventory |
| `chain-2-categorize-files.md` | Organize file structure | File categorization map |
| `chain-3-architecture.md` | Map architecture | Component relationships |
| `chain-4-domain-deep-dive.md` | Document domains | Domain knowledge base |
| `chain-5-style-guides.md` | Extract conventions | Style guides per file type |
| `chain-6-synthesis.md` | Create final instructions | `copilot-instructions.md` |

## Troubleshooting

### Chain outputs are too generic
- Add more specific examples to your prompt
- Reference specific files or directories
- Run the chain on a subdirectory first

### Chain misses important patterns
- Manually review and add to the synthesis step
- Provide corrections and re-run synthesis
- Update the chain prompt to explicitly look for those patterns

### Results don't match current codebase
- Re-run the chain - code may have evolved
- Update specific chain steps that are outdated
- Ensure Copilot is scanning the entire workspace

## Advanced: Customizing the Chain

You can modify these prompt files to:
- Add repository-specific steps
- Focus on particular domains
- Include additional context sources
- Integrate with your team's documentation

Simply edit the `.md` files to adjust what Copilot should look for and document.

## Next Steps

1. **Start with chain-1** - Run the first prompt to see how it works
2. **Continue sequentially** through all six steps
3. **Generate your instructions file** with chain-6
4. **Test with Copilot** to see improved code generation
5. **Iterate and refine** as needed

The investment in running this chain pays off with significantly better code suggestions that match your project's unique characteristics!
