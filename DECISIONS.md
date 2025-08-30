# Architectural Decision Records (ADRs)

This document tracks key architectural and design decisions made for the pantheon agentic systems project.

## ADR-001: XML vs JSON for Agent Specification Format

**Date**: 2025-08-21  
**Status**: Accepted  
**Context**: Need to choose a structured format for agent specifications and prompts

### Problem

When creating agent specifications for the agentic system creator, we needed to choose between XML and JSON for structuring agent definitions, constraints, workflows, and prompts.

### Decision

**Chosen**: XML format for agent specifications

### Rationale

#### Why XML was chosen over JSON:

1. **Mixed Content Support**
   - Agent specifications require both structured data AND natural language instructions
   - XML naturally handles mixed content (text + structure)
   - JSON requires escaping and string concatenation for multi-line text

2. **Human Readability and Self-Documentation**
   - XML tags like `<agent-role>`, `<constraints>`, `<workflow>` are semantically meaningful
   - Easier to scan and understand the document structure
   - Better for documentation that humans need to read and modify

3. **Natural Language Integration**
   - Agent prompts contain extensive free-form text and instructions
   - XML allows natural embedding of text content without escaping
   - Example comparison:
     ```xml
     <step id="1">
       <action>Collect System Information</action>
       <details>
         - Ask for the agentic system name
         - Validate the name for folder compatibility
       </details>
     </step>
     ```
     vs
     ```json
     {
       "step": {
         "id": "1",
         "action": "Collect System Information", 
         "details": "- Ask for the agentic system name\n- Validate the name for folder compatibility"
       }
     }
     ```

4. **Reference Consistency**
   - The existing `agentic-system-architect` agent uses a similar structured approach
   - XML format aligns better with established patterns in the codebase

5. **Agent Prompt Extraction**
   - Agent prompts need to be copied directly into Claude Code's Task tool
   - XML structure makes it easier to identify and extract the complete prompt
   - Clear boundaries between different sections of the specification

#### Trade-offs Considered

**XML Advantages:**
- Better for mixed content (text + structure)
- More readable for documentation
- Self-documenting tags
- Natural language friendly

**JSON Advantages:**
- More compact representation
- Native JavaScript/Python parsing
- Better for programmatic processing
- Familiar to most developers

### Implementation

Agent specifications use XML-style tags for:
- `<agent-role>` - Core agent purpose and expertise
- `<constraints>` with `<avoid>` - What the agent should not do
- `<expected-output>` with `<include>` - What the agent should produce
- `<workflow>` with `<step>` - Structured process steps
- `<examples>` with `<example>` - Usage examples
- `<features>` - Capability descriptions

Metadata (system config, agent registry) still uses JSON/YAML for programmatic processing.

### Consequences

**Positive:**
- Improved readability for agent specifications
- Easier maintenance of complex agent prompts
- Better documentation structure
- Consistent with existing patterns

**Negative:**
- Slightly more verbose than JSON
- Requires XML-aware tooling for programmatic processing
- Mixed format approach (XML for specs, JSON for config)

### Future Considerations

- Monitor if programmatic processing needs justify switching to JSON
- Consider hybrid approach: JSON for metadata, XML for prompts
- Evaluate tooling needs for XML processing if automation is required

---

## Future ADRs

Additional architectural decisions will be documented here as they arise.