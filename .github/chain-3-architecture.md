---
model: gpt-4.1
---

# Step 3: Identify the Architecture

Map how major pieces of the application fit together.

## Instructions

1. **Analyze the architecture patterns** used in this repository
2. **Document the major components** and their interactions
3. **Identify integration points** between services
4. **Map data flows** through the system

## Areas to Examine

### Application Architecture
- How are the samples structured?
- What architectural patterns are used (e.g., serverless, microservices)?
- How do components communicate?

### Authentication & Authorization Flow
- How is authentication handled?
- Where does authorization occur?
- What security patterns are implemented?

### Data Layer
- How is data stored and accessed?
- What data persistence patterns are used?
- How are FHIR resources managed?

### API & Integration Layer
- What API patterns are used?
- How are external services integrated?
- What middleware or gateways are present?

### Frontend (if applicable)
- How is the UI structured?
- What state management is used?
- How does frontend communicate with backend?

### Deployment Architecture
- How are services deployed?
- What cloud architecture patterns are used?
- How is infrastructure provisioned?

## Output Format

### High-Level Architecture

```
[Describe the overall architecture, e.g.:]
- API Gateway (APIM) routes requests
- Azure Functions handle SMART on FHIR operations
- FHIR Service stores healthcare data
- Entra ID provides authentication
- Key Vault secures secrets
```

### Component Interactions

For each major component:
- **Name**: Component name
- **Purpose**: What it does
- **Dependencies**: What it depends on
- **Consumers**: What depends on it
- **Integration Pattern**: How it integrates

### Data Flow Diagrams

Describe key flows:
1. Authentication flow
2. FHIR resource access flow
3. Bulk export flow
4. etc.

This architectural understanding guides how new code should integrate with existing systems.
