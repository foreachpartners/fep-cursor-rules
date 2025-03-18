# Cursor Rules Requirements

## Priority Legend

- **P0** - Must implement (critical)
- **P1** - Should implement (high importance)
- **P2** - Recommended (medium importance)
- **P3** - Consider when possible (lower importance)

All rules must include this legend and apply these priority levels consistently.

## I. Technical Requirements (P0)

### 1. Format Standards

- Use valid Markdown, checked with markdownlint (DavidAnson.vscode-markdownlint)
- Include YAML frontmatter with description, globs, and related files
- Include priority legend in all main documents
- Apply priority indicators (P0-P3) consistently
- Write all rules in English only

### 2. Size Constraints

- **Rules Guide**: 150-250 lines (~5-7K tokens)
- **Specific Rule**: 300-500 lines (~10-15K tokens)
- **Context Budget**: Rules ≤20% of context window
- **Examples**: 5-10 lines per code snippet

### 3. Structure

- Use hierarchical organization with clear headings
- Place critical content at document beginning
- Prefer lists over paragraphs
- Implement cross-references between related rules
- Use glob patterns for automatic rule loading

### 4. Rules Guide

- Create concise overview (1-2 pages)
- Include clear references to detailed documents
- Provide navigation guides for LLMs

## II. Development Process (P1)

### 1. Workflow

1. Assess user preferences and priorities
2. Collect input on all technical aspects
3. Prioritize based on project needs
4. Implement in priority order
5. Validate with LLM testing

### 2. Coverage (Prioritized)

- **Must Have**: Code Structure, Architecture Design, Types, Errors, Testing, Dependencies, Style, Documentation, String Literals, Constants, Configuration, Logging
- **Should Have**: Framework Patterns, Integration, Developer Experience
- **Nice to Have**: Performance, Security

### 3. Explicitly Low Priority

- DevOps/CI/CD
- Advanced optimizations
- Enterprise security features
- Monitoring systems
- Future-proofing architecture

## III. Quality Requirements (P2)

- Use unambiguous, direct language
- Make rules specific to technology stack
- Balance comprehensiveness with brevity
- Avoid overly restrictive guidelines

## IV. LLM Optimization (P2)

- Optimize token usage with concise language
- Use explicit patterns (Always X / Never Y)
- Provide minimal but sufficient examples
- Include self-verification mechanisms

## V. Maintenance (P3)

- Version and date all documents
- Design for adaptability to technology changes
- Include success criteria and metrics

## VI. Coverage Details (P3)

Each technical aspect should address:

1. **Code Structure**: Project organization, imports, naming
2. **Architecture**: Design principles, dependencies, patterns
3. **Types**: Type system, interfaces, type safety
4. **Errors**: Exception handling, graceful degradation
5. **Testing**: Unit/integration approaches, mocking
6. **Dependencies**: Package management, versioning
7. **Style**: Formatting, naming conventions
8. **Documentation**: Code docs, API docs, README
9. **Framework**: Framework-specific patterns and practices
10. **Integration**: APIs, third-party services, databases
11. **Logging**: Log levels, structured logging
12. **Configuration**: Env vars, config files, secrets
13. **Performance**: Resource management, optimization
14. **Security**: Input validation, auth patterns
15. **Developer**: IDE setup, linting, workflow
