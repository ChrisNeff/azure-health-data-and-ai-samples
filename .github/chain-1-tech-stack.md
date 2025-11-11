# Step 1: Determine the Tech Stack

Analyze this repository and identify all languages, frameworks, and libraries in use.

## Instructions

1. **Scan the entire codebase** to discover all technologies used
2. **Categorize findings** into:
   - **Primary Languages**: (e.g., C#, TypeScript, Python, PowerShell)
   - **Frameworks**: (e.g., .NET 8, Azure Functions, Blazor)
   - **Major Libraries**: (e.g., FHIR.NET, xUnit, NSubstitute)
   - **Azure Services**: (e.g., Azure Health Data Services, APIM, Key Vault)
   - **Build Tools**: (e.g., Azure Developer CLI, Bicep)
   - **Package Managers**: (e.g., NuGet, npm)

3. **Document versions** where specified in project files

4. **Note any monorepo patterns** or multiple projects with different stacks

## Output Format

Provide a structured list:

### Primary Languages
- Language and usage percentage

### Frameworks & Runtime
- Framework name and version
- Purpose in the project

### Key Libraries & Dependencies
- Library name, version, and purpose

### Azure Services
- Service name and role

### Infrastructure & DevOps
- Tools and their purpose

This output will be used as foundational context for the remaining chain steps.
