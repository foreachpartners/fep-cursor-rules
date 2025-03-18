# Requirements for Quality Cursor Rules

## Core Requirements

### 1. Clarity and Precision

- Rules must be unambiguous and leave no room for interpretation
- Use direct, imperative statements rather than suggestions
- Avoid metaphors and language that can be interpreted in multiple ways
- Specify exact requirements rather than general guidance

### 2. Structure and Organization

- Organize rules in logical categories (formatting, architecture, testing, etc.)
- Use consistent formatting and hierarchy throughout
- Employ a standardized template for all rule types
- Include clear headers and subheaders for navigation

### 3. Contextual Relevance

- Rules must be specific to the technology stack
- Include explicit conditions for when rules apply
- Address edge cases and exceptions
- Adjust detail level based on criticality (more detail for critical aspects)

### 4. Balance

- Strike balance between comprehensiveness and brevity
- Prioritize rules based on importance and impact
- Avoid overly restrictive rules that limit innovation
- Ensure rules promote quality without excessive constraints

## LLM-Specific Requirements

### 1. Token Optimization

- Critical rules should appear earlier in the document
- Keep individual rules concise to maximize tokens for content
- Use efficient language that minimizes token usage
- Structure information to fit within model context limits

### 2. Explicit Patterns

- Use consistent patterns like "Always X / Never Y / If A then B"
- Structure rules in predictable formats that LLMs can easily follow
- Employ clear demarcation between different rule types
- Use standard indicators for priorities (P0, P1, P2)

### 3. Learning Through Examples

- Include concrete examples of correct implementation
- Provide counter-examples of incorrect implementation
- Use minimal but sufficient context in examples
- Follow examples with explicit explanation of principles applied

### 4. Self-Verification

- Include mechanisms for the LLM to verify rule application
- Add distinct markers to identify which rules are being applied
- Create verification commands that trigger rule diagnosis
- Design test prompts to confirm understanding of rules

## Technology-Specific Requirements

### 1. Framework Alignment

- Rules must align with framework best practices
- Address framework-specific patterns and anti-patterns
- Include rules for framework-specific tooling
- Update as framework versions and recommendations evolve

### 2. Ecosystem Integration

- Address common libraries and tools within each ecosystem
- Include rules for testing frameworks specific to the stack
- Cover deployment and environment considerations
- Address performance optimizations unique to the stack

### 3. Community Standards

- Incorporate established community conventions
- Align with published style guides for the technology
- Reference authoritative sources for recommendations
- Maintain compatibility with linting and formatting tools

## Maintenance Requirements

### 1. Versioning

- Include version number and last updated date
- Document changes between versions
- Maintain backward compatibility where possible
- Clearly mark deprecated rules

### 2. Adaptability

- Design rules to accommodate future changes in technology
- Include principles that transcend specific implementations
- Create extension points for project-specific customizations
- Separate timeless rules from technology-specific guidance

### 3. Measurability

- Define success criteria for rule implementation
- Include metrics to evaluate rule effectiveness
- Provide mechanisms to track rule adherence
- Enable quantitative feedback on rule usefulness

## Required Coverage Aspects

Based on analysis of existing Python and Next.js rules, effective Cursor Rules should cover these technical aspects:

### 1. Code Structure and Organization

- Project directory structure and file organization
- Module and package organization
- Component hierarchy (UI frameworks)
- File naming conventions and locations
- Import/export patterns

### 2. Architectural Patterns

- Design principles (DRY, SOLID, etc.)
- Layered architecture approaches
- Separation of concerns
- Dependency direction and management
- State management patterns

### 3. Typing and Type Safety

- Type system usage and conventions
- Generic types and type parameters
- Interface/type definitions
- Type guards and narrowing
- Type inference optimization

### 4. Error Handling

- Exception/error hierarchies
- Error propagation patterns
- Retry mechanisms
- Graceful degradation strategies
- Logging integration with errors

### 5. Testing Strategies

- Unit/integration/E2E testing approaches
- Test organization and naming
- Mocking strategies
- Test data management
- Coverage requirements

### 6. Performance Optimization

- Resource management
- Caching strategies
- Lazy loading patterns
- Rendering optimization
- Bundle size management

### 7. Security Practices

- Input validation
- Authentication/authorization patterns
- Data sanitization
- Secure API access
- Environment variable management

### 8. Developer Experience

- IDE configuration
- Code formatting and linting
- Documentation requirements
- Debugging practices
- Development workflow

### 9. Framework-Specific Patterns

- Routing and navigation
- Data fetching strategies
- Component lifecycle management
- Server/client code separation
- Framework feature utilization

### 10. Integration Points

- API service layer organization
- Third-party library integration
- External service communication
- Database access patterns
- Content management

### 11. Dependency Management

- Package manager conventions (npm, pnpm, yarn, uv, pip, etc.)
- Dependency versioning strategy
- Monorepo management (if applicable)
- Dependency update policies
- Local dependency management

### 12. Code Style Guidelines

- Formatting conventions
- Naming conventions
- Comment style and requirements
- File structure templates
- Code organization within files

### 13. Documentation Standards

- Code documentation (docstrings, JSDoc, etc.)
- API documentation
- Architecture documentation
- README and contributor guidelines
- Changelog maintenance

### 14. Logging Framework

- Logging levels and when to use them
- Structured logging patterns
- Log rotation and management
- Contextual logging
- Error correlation in logs

### 15. Configuration Management

- Environment variables usage
- Configuration file structures
- Secret management
- Feature flags
- Environment-specific configurations

## Master Rules Document

Each technology stack should include a master rules document with these characteristics:

- Extremely concise overview of all rules (maximum 1-2 pages)
- Clear references to detailed rule documents
- Hierarchical organization mirroring the rule structure
- Priority indicators for each rule section
- Quick reference for the most critical rules
- Navigation guides for LLM to find detailed information

## Low-Priority Aspects

The following aspects are explicitly defined as low-priority in our rules:

### 1. DevOps Concerns

- CI/CD pipelines
- Deployment strategies
- Infrastructure as code
- Container orchestration
- Release automation

### 2. Advanced Performance Optimization

- Micro-optimizations
- Extreme performance tuning
- Framework-specific performance tricks
- Database query optimization
- Network protocol optimization

### 3. Enterprise-level Security

- Advanced security hardening
- Penetration testing
- Security certification compliance
- Cryptographic implementations
- Zero-trust architecture

### 4. Advanced Monitoring

- APM integration
- Metric collection systems
- Dashboard creation
- Alerting systems
- Log aggregation

### 5. Future-proof Architecture

- The rules prioritize simplicity over future-proofing
- Architecture should solve current problems efficiently
- Avoid speculative generalization
- Minimize abstractions not immediately needed
- Focus on maintainability of current codebase

## File Size and Structure Requirements

To ensure optimal performance with LLMs like Claude 3.7 Sonnet while allowing sufficient context space for code, documentation, and search results, the following size constraints should be observed:

### Size Constraints

- **Master Rules Document**: 150-250 lines (approximately 5-7K tokens)
- **Specialized Rule Files**: 300-500 lines (approximately 10-15K tokens)
- **Total Rules in Context**: Not to exceed 40K tokens (approximately 20% of context window)
- **Example Code Snippets**: Limit to 5-10 lines per example
- **Rule Modules**: Aim for logical modules of 200-400 lines each

### Structure Optimization

1. **Hierarchical Organization**
   - Prioritize rules by frequency of application
   - Place critical rules at the beginning of documents
   - Use clear section headers for navigation
   - Implement reference links between related rules

2. **Format Efficiency**
   - Use bulleted lists instead of lengthy paragraphs
   - Employ tables for compact representation of related rules
   - Apply consistent formatting throughout all rule files
   - Use headings and subheadings for clear visual hierarchy

3. **Context Optimization**
   - Minimize redundancy across rule files
   - Use cross-references instead of duplicating content
   - Provide minimal but sufficient context in examples
   - Highlight key code patterns rather than complete implementations

### Modular Loading Strategy

1. **File Pattern Matching**
   - Leverage glob patterns to automatically include relevant rules
   - Configure rules to match specific file extensions or directories
   - Ensure rules are loaded only when needed based on active files

2. **Depth on Demand**
   - Include essential rules in every context
   - Load detailed rules only when specific topics are addressed
   - Use semantic descriptions for intelligent rule application
   - Implement priority levels for rule application

3. **Context Sharing**
   - Consider context allocation between rules and other content:
     - Source code: ~50% of context
     - Search results and documentation: ~30% of context
     - Conversation history: ~5% of context
     - Rules: ~15-20% of context
