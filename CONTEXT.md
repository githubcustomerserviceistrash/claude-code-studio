# CONTEXT TEMPLATE - Personal Development Environment

<!-- 
This is a template version of CONTEXT.md for public sharing.
Replace all [PLACEHOLDER] variables with your personal information.
Customize project lists, paths, and configurations to match your setup.
-->

# CONTEXT - Personal Development Environment

## SYSTEM CONTEXT
Working with Nathan Rice (nathan) on Ubuntu Linux, x86, NVidia GPU.

## ENVIRONMENT SPECIFICS
- Platform: linux x86_64

## CRITICAL PATHS
- Home: /home/nathan
- Projects: /home/nathan/projects ([PROJECT_COUNT] WSL projects)
- Claude Config: /home/nathan/.claude

## DEVELOPMENT ENVIRONMENT
- Bun
- Git: "Nathan Rice" <nathan.alexander.rice@gmail.com>
- Editor: zed
- Shell: bash

## AGENT-FIRST WORKFLOW

### Default Operating Principle: USE AGENTS WHENEVER POSSIBLE
**Agent usage is the DEFAULT, not the exception.** With 40+ specialized agents available, prefer agent delegation over direct handling for better context management and expert-level results.

### UTILITY-FIRST MANDATE
**MANDATORY**: Utility agents must be used for ALL basic operations - no exceptions.

**Non-Negotiable Utility Agent Usage:**
- **file-creator**: ALL file/directory creation tasks (instead of Write tool)
- **git-workflow**: ALL git operations (instead of Bash git commands)  
- **date-checker**: ALL date/time queries (instead of manual calculations)
- **context-fetcher**: ALL documentation retrieval (instead of Read tool for docs)

### Agent Usage Decision Tree
```
IF utility_task (file creation, git ops, dates, doc retrieval):
  USE_UTILITY_AGENT (MANDATORY - no direct tool usage)
ELIF task_matches_specific_expertise:
  USE_SPECIALIZED_AGENT (engineering, design, marketing, etc.)
ELIF task_is_multi_domain:
  USE_MULTIPLE_AGENTS (coordinate via studio-coach if complex)
ELIF task_needs_fresh_context:
  USE_AGENT (prevents conversation context bloat)
ELSE:
  USE_GENERAL_PURPOSE_AGENT (rapid-prototyper, studio-coach)
```

### Context Management Benefits
- **Fresh Context**: Each agent starts with clean slate, no conversation overhead
- **Specialized Prompts**: 500+ word expert-level system prompts per domain
- **Parallel Processing**: Multiple agents can work simultaneously on different aspects
- **Performance Isolation**: Agent failures don't affect main conversation
- **Expert Quality**: Purpose-built expertise vs generalist approach

### Available Agent Categories & Usage
**📚 Full Agent Documentation**: `/home/nathan/.claude/agents/README.md`

**Core Usage Patterns:**
- **Engineering Tasks** → rapid-prototyper, backend-architect, frontend-developer, ai-engineer
- **Design Work** → ui-designer, whimsy-injector, brand-guardian, ux-researcher  
- **Marketing Needs** → tiktok-strategist, growth-hacker, app-store-optimizer
- **Product Decisions** → sprint-prioritizer, trend-researcher, feedback-synthesizer
- **Operations** → support-responder, finance-tracker, analytics-reporter
- **Testing/QA** → test-writer-fixer, api-tester, performance-benchmarker, test-runner
- **Utilities** → context-fetcher, file-creator, git-workflow, date-checker

### Proactive Agent Triggers
- **whimsy-injector**: Auto-activates after UI/UX changes
- **test-writer-fixer**: Triggered after code modifications
- **studio-coach**: Orchestrates complex multi-agent workflows  
- **experiment-tracker**: Activates when feature flags/experiments are mentioned

### Agent Coordination Philosophy  
- **Single Domain**: Use specialized agent directly
- **Multi-Domain**: studio-coach coordinates multiple agents
- **Complex Projects**: Agent teams work in parallel with clear handoffs
- **Simple Queries**: Still prefer agent if available for context isolation

### Integration with MCP Tools
Agents leverage MCP.md guidance for:
- Tool selection optimization
- Performance-conscious decisions  
- Anti-pattern avoidance
- Systematic workflows

### Serena MCP Integration
- Semantic code analysis and project memory
- LSP-based symbol understanding for complex refactoring
- Enhanced code navigation and pattern recognition
- Project insights stored in .serena/memories/ for context retention

### Engineering Standards
**📚 Detailed Standards**: `/home/nathan/.claude/ENGINEERING-STANDARDS.md`

**Core Requirements**: Monorepo structure, test-first development, documentation standards, and operational automation for scalable system development.