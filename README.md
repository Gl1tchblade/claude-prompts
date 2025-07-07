# Claude Code Prompts
> [!IMPORTANT]
> These prompts are designed to work effectively but please use them with caution and review any code you ship to production
## Prompts
- [Multi-agent](https://github.com/Gl1tchblade/claude-prompts/blob/main/multi-agent.md)
- More to come :)
## How to use
1. Take a prompt you like and copy it like [Multi-agent](https://github.com/Gl1tchblade/claude-prompts/blob/main/multi-agent.md)
2. Run the command `nano ./claude/commands/prompt-name.md` (For this example you would put multi-agent.md)
3. Paste in the prompt
4. Click `Ctrl + X` then `y` and finally `enter`
5. Go to a directory where you want to run claude code
6. Run claude code through the `claude` command
7. Once you see it load in type `/prompt-name [YOUR TASK HERE]` (For the multi-agent example you would type `/multi-agent` and then your task
8. Once you typed task you can click enter and watch claude code work!
> [!Warning]
> By default it will commit code it writes once it's done so if you want to disable this just add to your prompt `Do not commit any code I will do this myself if needed`

## Breakdown of prompts

### [Multi-agent](https://github.com/Gl1tchblade/claude-prompts/blob/main/multi-agent.md)
The multi-agent prompt transforms Claude into an **Autonomous Orchestration Agent** that breaks down complex coding tasks into manageable sub-tasks and executes them in parallel. Here's how it works:

**Core Process:**
1. **Task Analysis** - Analyzes your codebase and the complex task you've given it
2. **Smart Decomposition** - Breaks the large task into 3-7 independent sub-tasks that can run in parallel
3. **Creates Task Folder** - Generates a structured folder with naming like `Feature - Task Name - 2025-07-07`
4. **Generates Individual Plans** - Creates detailed markdown files for each sub-task with:
  - Mission briefs and implementation guidelines
  - Todo checklists for analysis, design, implementation, testing, and documentation
  - Risk assessments and testing strategies
5. **Master Coordination** - Creates an `info.md` file with:
  - Overall strategy and detected technical guidelines
  - Git protocols for coordination between sub-agents
  - Dependencies and collaboration rules
6. **Parallel Execution** - Launches ALL independent sub-tasks simultaneously as a batch operation
7. **Centralized Git Management** - Reviews and commits each sub-task's work separately with proper commit messages

**Key Features:**
- **True Parallelism**: Independent tasks run simultaneously, not sequentially
- **Dependency Management**: Handles task dependencies intelligently
- **Git Protocol**: Centralized commit management prevents conflicts
- **Adaptive Technology Detection**: Automatically detects your project's tech stack and follows existing patterns
- **Quality Control**: Each sub-task includes comprehensive testing and review steps

This approach is perfect for large features, refactoring projects, or any complex development task that can benefit from parallel execution and systematic coordination.
