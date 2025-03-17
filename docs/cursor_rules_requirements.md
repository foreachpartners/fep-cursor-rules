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
