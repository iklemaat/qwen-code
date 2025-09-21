# Agent Patterns for Qwen Code

This documentation presents the 5 agent patterns to simplify development with Qwen Code, from simple interactions to complex, complete solutions. Each pattern addresses specific needs in an AI engineer's workflow, providing tools to scale automation incrementally and controllably.

## Table of Contents

1. [Introduction](#introduction)
2. [Pattern 1: Iterative Human-in-the-Loop (HILL)](#pattern-1-iterative-human-in-the-loop-hill)
3. [Pattern 2: Reusable Prompts (Custom Commands)](#pattern-2-reusable-prompts-custom-commands)
4. [Pattern 3: Sub Agents](#pattern-3-sub-agents)
5. [Pattern 4: Wrapper MCP Server](#pattern-4-wrapper-mcp-server)
6. [Pattern 5: Full Application (Complete Application)](#pattern-5-full-application-complete-application)
7. [Complexity and Applicability Hierarchy](#complexity-and-applicability-hierarchy)
8. [Decision Framework for Pattern Selection](#decision-framework-for-pattern-selection)
9. [Implementation Recommendations](#implementation-recommendations)

## Introduction

The following documentation outlines five agent patterns for simplifying agentic coding workflows. These patterns represent a logical progression from simple interactions to complex, complete solutions. Each pattern addresses specific needs in an AI engineer's workflow, providing tools to scale automation incrementally and controllably.

## Pattern 1: Iterative Human-in-the-Loop (HILL)

### Description
This pattern represents the most basic form of interaction between human and agent, where each step requires direct manual supervision and validation.

### Key Characteristics
- **Direct Supervision**: Constant and explicit human control over each action
- **Simplicity**: Easy to understand and implement
- **High Precision/Control**: Allows fine adjustments in real-time
- **Low Scalability**: Human is the bottleneck of the process
- **Ideal Starting Point**: Perfect for exploring new solutions or complex problems

### Use Case Context
- New problems without established solutions
- Tasks requiring critical validation at each step
- Rapid prototyping and experimentation
- Situations where human error is costly

## Pattern 2: Reusable Prompts (Custom Commands)

### Description
This pattern encapsulates effective prompts into reusable commands, creating "recipes" for common tasks that can be executed repeatedly.

### Key Characteristics
- **Reusability**: Single definition for multiple uses
- **Version Control**: Management like any other code
- **Pareto Efficiency (80/20)**: Greatest value for time invested
- **Initial Automation**: First step toward reducing manual intervention
- **Configuration Overhead**: Requires organization and maintenance

### Use Case Context
- Tasks repeated three or more times
- Standardized processes with minimal variations
- Team needing to share effective solutions
- Reduction of errors due to prompt inconsistency

## Pattern 3: Sub Agents

### Description
Introduces the capability to delegate specialized tasks to sub-agents that can run in parallel, allowing for more efficient division of responsibilities.

### Key Characteristics
- **Specialization**: Each sub-agent focuses on a specific task
- **Parallelization**: Simultaneous execution of multiple tasks
- **Interaction with External Services**: Structured integration with APIs
- **Context Window Management**: Isolation of information by context
- **Information Flow Complexity**: Requires careful management of data between agents
- **Tool Dependency**: Requires specific platform support

### Use Case Context
- Complex tasks that can be divided into subtasks
- Need for parallel processing
- Integration with multiple services or APIs
- Technical specialization requirements

## Pattern 4: Wrapper MCP Server

### Description
Provides a centralized interface layer that acts as a bridge between agents and various services, encapsulating integration logic in a custom server.

### Key Characteristics
- **Unified Interface Layer**: Single access point to complex functionalities
- **Integration Centralization**: Simplification of managing multiple services
- **Total Control and Customization**: Precise definition of interactions
- **Workflow Exposure**: Custom commands for complex processes
- **Proprietary Service Integration**: Access to internal systems not directly accessible
- **Continuous Maintenance**: Requires ongoing updates and care
- **Manual Construction**: Integration logic must be explicitly developed

### Use Case Context
- Integration with proprietary or internal systems
- Need for specific control over service interactions
- Complex workflows combining multiple tools
- Security or controlled access requirements

## Pattern 5: Full Application (Complete Application)

### Description
The most advanced pattern involving building a complete software product with multiple interface layers and functionality.

### Key Characteristics
- **Total Control**: Maximum freedom to define functionalities
- **Infinitely Extensible**: Ability to add any feature
- **Multiple Access Patterns**: Integrated CLI, UI, API, and MCP
- **Long-Term Vision**: Justified for products or organizational solutions
- **High Cost/Complexity**: Greater investment of time and resources
- **Overqualification**: Excess for most agent problems
- **Complete Framework**: Integral solution for complex needs

### Use Case Context
- Complete software product development
- Large-scale organizational solutions
- Multiple user interface needs
- Requirements for total control over all functionalities

## Complexity and Applicability Hierarchy

### Technical Complexity Level
1. **HILL**: Very low - Direct interaction
2. **Reusable Prompts**: Low - Prompt encoding
3. **Sub Agents**: Medium - Managing multiple agents
4. **Wrapper MCP**: High - Custom server development
5. **Full Application**: Very high - Complete product development

### Scalability
1. **HILL**: Low - Limited by human capacity
2. **Reusable Prompts**: Medium - Improves individual efficiency
3. **Sub Agents**: High - Parallelization and specialization
4. **Wrapper MCP**: High - Service centralization
5. **Full Application**: Maximum - Complete architecture

### Value Provided
1. **HILL**: Low for repetitive tasks, high for new solutions
2. **Reusable Prompts**: High - Best value/time ratio
3. **Sub Agents**: High - For complex and parallelizable tasks
4. **Wrapper MCP**: High - For complex integrations
5. **Full Application**: Variable - Only justified for products

## Decision Framework for Pattern Selection

### Decision Tree
1. **Is this a new or exploratory problem?**
   - **YES** → HILL Pattern
   - **NO** → Continue

2. **Does the task repeat 3 or more times?**
   - **NO** → Remain in HILL Pattern
   - **YES** → Continue

3. **Can it be divided into independent subtasks?**
   - **NO** → Reusable Prompts Pattern
   - **YES** → Continue

4. **Does it require parallel processing?**
   - **NO** → Reusable Prompts Pattern
   - **YES** → Continue

5. **Does it need to integrate with external systems?**
   - **NO** → Sub Agents Pattern
   - **YES** → Continue

6. **Is there a long-term product vision?**
   - **NO** → Wrapper MCP Server Pattern
   - **YES** → Full Application Pattern

## Implementation Recommendations

### Progressive Implementation
1. **Start with HILL** for new and exploratory problems
2. **Evolve to Reusable Prompts** when repetitive tasks are identified
3. **Advance to Sub Agents** for complex divisible problems
4. **Consider Wrapper MCP Server** for complex integrations
5. **Only implement Full Application** with a clear product vision

### Strategic Considerations
- **Keep It Simple**: Start with the simplest pattern that solves the problem
- **Scale When Necessary**: Only increase complexity when the problem demands it
- **Avoid Overengineering**: Don't implement complex solutions for simple problems
- **Plan for the Future**: Consider natural evolution of patterns

This documentation provides a comprehensive guide to understanding, selecting, and implementing the 5 agent patterns in Qwen Code, enabling AI engineers to optimize their workflow.