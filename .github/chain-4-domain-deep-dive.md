# Step 4: Domain Deep Dive

Document specific domains using real code examples from the project.

## Instructions

1. **Identify the key domains** in this healthcare/FHIR repository:
   - SMART on FHIR authentication
   - FHIR resource operations
   - Healthcare data standards (FHIR R4/R5, US Core)
   - Azure Health Data Services integration
   - Bulk data operations
   - Terminology services
   - Analytics and reporting

2. **For each domain**, provide:
   - Core concepts and terminology
   - Real code examples from the repository
   - Common patterns used
   - Domain-specific rules and constraints

## Domains to Document

### SMART on FHIR Domain

**Concepts**: OAuth 2.0, scopes, launch contexts, authorization flows

**Code Examples**:
- Find actual scope parsing code
- Find authorization handlers
- Find token management code

**Patterns**:
- How are SMART scopes validated?
- How is launch context maintained?
- How are tokens refreshed?

**Rules**:
- What SMART specifications are followed?
- What scope formats are supported?
- What security constraints exist?

### FHIR Resource Management Domain

**Concepts**: Resources, bundles, search parameters, operations

**Code Examples**:
- Find FHIR client usage
- Find resource CRUD operations
- Find search implementations

**Patterns**:
- How are FHIR clients initialized?
- How are resources validated?
- How are bundles processed?

**Rules**:
- What FHIR version(s) are supported?
- What profiles are implemented?
- What validation is required?

### Azure Integration Domain

**Concepts**: Managed identities, Key Vault, APIM policies, Function Apps

**Code Examples**:
- Find Azure SDK usage
- Find authentication patterns
- Find service integration code

**Patterns**:
- How are Azure services accessed?
- How are secrets managed?
- How is retry logic implemented?

**Rules**:
- What security practices are mandatory?
- What logging patterns are used?
- What error handling is required?

### Testing Domain

**Concepts**: xUnit, NSubstitute, test patterns, AAA structure

**Code Examples**:
- Find representative test files
- Find mocking patterns
- Find assertion patterns

**Patterns**:
- How are tests structured?
- How are dependencies mocked?
- How are async operations tested?

**Rules**:
- What test naming convention is used?
- What test structure is required?
- What mocking library is used?

## Output Format

For each domain:

### Domain Name

**Purpose**: What this domain covers

**Key Concepts**: List of important terms and concepts

**Real Examples** (with file references):
```csharp
// From: samples/.../AuthorizeFunction.cs
[Actual code snippet from repository]
```

**Common Patterns**:
1. Pattern name: Description and when to use
2. Pattern name: Description and when to use

**Rules & Constraints**:
- Rule 1: Specific requirement
- Rule 2: Specific requirement

Pull real code examples directly from the repository to ground the domain knowledge in actual implementation.
