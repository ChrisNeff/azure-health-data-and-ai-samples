# Step 2: Categorize the Files

Organize every file in the repository by purpose and type.

## Instructions

1. **Scan all directories** and analyze file patterns
2. **Group files** into functional categories:
   - **Source Code**: Controllers, Services, Models, Functions, etc.
   - **Tests**: Unit tests, integration tests, test fixtures
   - **Infrastructure**: Bicep files, ARM templates, deployment scripts
   - **Configuration**: appsettings.json, parameters files, yaml configs
   - **Documentation**: README files, markdown docs, diagrams
   - **Build & CI/CD**: GitHub workflows, build scripts
   - **Data**: Sample data, test data, seed files
   - **Frontend**: Components, pages, styles (if applicable)

3. **Identify naming patterns** for each category
4. **Note directory structure conventions**

## Output Format

Create a hierarchical categorization:

### /samples/{sample-name}/
- **Purpose**: [What this sample demonstrates]
- **Structure**:
  - `/src/` - Source code
  - `/infra/` - Infrastructure as code
  - `/tests/` - Test projects
  - `/docs/` - Documentation
  - `/scripts/` - Deployment/utility scripts

### File Type Categories

#### Azure Functions (*.cs in Function projects)
- Location pattern: `/src/**/*.Functions/`
- Purpose: Serverless compute handlers
- Common names: AuthorizeFunction, TokenFunction, etc.

#### Bicep Templates (*.bicep)
- Location pattern: `/infra/**/*.bicep`
- Purpose: Infrastructure definitions
- Common names: main.bicep, fhir.bicep, etc.

#### Unit Tests (*Tests.cs)
- Location pattern: `/src/**/*.UnitTests/`
- Purpose: Test coverage
- Naming: {ClassUnderTest}Tests.cs

[Continue for all file categories found]

This categorization will inform code generation patterns in later steps.
