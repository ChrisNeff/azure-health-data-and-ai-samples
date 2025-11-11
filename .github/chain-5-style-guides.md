# Step 5: Generate Style Guides

Capture unique conventions that define this codebase for each file type.

## Instructions

1. **Analyze existing code** to extract actual patterns used
2. **Document conventions** for each file type
3. **Provide real examples** from the codebase
4. **Note mandatory vs. preferred** patterns

## File Types to Document

### C# Source Files

**File Header**:
```csharp
// [Extract actual header pattern from repo]
```

**Naming Conventions**:
- Classes: PascalCase
- Methods: PascalCase
- Variables: camelCase
- Private fields: _camelCase
- Constants: PascalCase

**Code Structure**:
- Using statements order
- Class organization (fields, properties, constructors, methods)
- Async/await patterns
- Exception handling patterns

**Real Examples**:
```csharp
// From: [actual file path]
[Actual code showing the pattern]
```

### C# Test Files

**File Header**:
```csharp
// -------------------------------------------------------------------------------------------------
// Copyright (c) Microsoft Corporation. All rights reserved.
// Licensed under the MIT License (MIT). See LICENSE in the repo root for license information.
// -------------------------------------------------------------------------------------------------
```

**Naming Conventions**:
- Test class: `{ClassUnderTest}Tests`
- Test method: `Given{Context}_When{Action}_Then{ExpectedOutcome}`

**Structure**:
- AAA pattern (Arrange-Act-Assert)
- Use NSubstitute for mocking
- Use xUnit attributes and assertions

**Real Examples**:
```csharp
// From: [actual test file path]
[Actual test showing the pattern]
```

### Bicep Infrastructure Files

**File Organization**:
- Parameters at top with descriptions
- Variables section
- Resources section
- Outputs at bottom

**Naming Conventions**:
- Parameters: camelCase
- Variables: camelCase
- Resources: descriptive names

**Patterns**:
- Use @description decorators
- Use @allowed for constrained values
- Use modules for reusability

**Real Examples**:
```bicep
// From: [actual bicep file path]
[Actual bicep showing the pattern]
```

### PowerShell Scripts

**File Header**:
```powershell
<#
.SYNOPSIS
    [Pattern used in repo]
#>
```

**Conventions**:
- Approved verbs (Get-, Set-, New-, etc.)
- Parameter validation
- Error handling with try/catch
- Verbose output support

**Real Examples**:
```powershell
# From: [actual script path]
[Actual script showing the pattern]
```

### Markdown Documentation

**Structure**:
- Clear hierarchy with headers
- Code blocks with language specification
- Bulleted lists for steps
- Links to related documentation

**Conventions**:
- README structure (Purpose, Prerequisites, Deployment, Usage)
- Architecture diagram placement
- Reference link formatting

### JSON Configuration Files

**Formatting**:
- 2 or 4 space indentation (based on what's used)
- Property naming conventions
- Comment handling (if supported)

## Output Format

For each file type:

### File Type: [Name]

**Purpose**: What this file type is used for

**Mandatory Conventions**:
1. Convention: Requirement (with example)
2. Convention: Requirement (with example)

**Preferred Patterns**:
1. Pattern: When and why to use (with example)
2. Pattern: When and why to use (with example)

**Anti-Patterns** (what to avoid):
1. Anti-pattern: Why it's problematic
2. Anti-pattern: Why it's problematic

**Real Example**:
```
// From: [file path]
[Complete, real example from the repository]
```

Extract actual patterns from the codebase rather than generic style guides. The goal is to match the existing code's style perfectly.
