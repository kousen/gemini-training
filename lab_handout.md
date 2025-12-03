# Gemini CLI Training Labs

This document contains hands-on exercises for learning to use Gemini CLI for professional development workflows.

## Table of Contents

0. [Lab 0: Project Creation from Scratch](#lab-0-project-creation-from-scratch)
1. [Lab 1: First Steps with Gemini CLI](#lab-1-first-steps-with-gemini-cli)
2. [Lab 2: Code Exploration](#lab-2-code-exploration)
3. [Lab 3: GEMINI.md and Context Management](#lab-3-geminimd-and-context-management)
4. [Lab 4: Test Generation](#lab-4-test-generation)
5. [Lab 5: Configuration and Safety](#lab-5-configuration-and-safety)
6. [Lab 6: Advanced Features](#lab-6-advanced-features)

## Prerequisites

- Gemini CLI installed: `npm install -g @google/gemini-cli`
- API key set: `export GEMINI_API_KEY="your-key"`
- Git installed and configured
- Development environment for Python, JavaScript, or Java
- Docker (optional, for sandbox mode)

---

## Lab 0: Project Creation from Scratch

**Duration**: 20 minutes

**Goal**: Create a task manager application from nothing using Gemini CLI

### Setup

1. Create a new empty directory:
   ```bash
   mkdir task-manager && cd task-manager
   ```

2. Initialize git:
   ```bash
   git init
   ```

3. Start Gemini CLI:
   ```bash
   gemini
   ```

### Exercises

1. **Project foundation**:
   ```
   Create a Node.js task manager application with:
   - A Task class with id, title, description, status, and dueDate
   - Functions to add, remove, update, and list tasks
   - JSON file storage for persistence
   - A simple CLI interface using readline
   ```

2. **Enhanced functionality**:
   ```
   Add these features to the task manager:
   - Filter tasks by status (pending, in-progress, completed)
   - Sort tasks by due date
   - Search tasks by title or description
   - Colored console output for different statuses
   ```

3. **Testing**:
   ```
   Create comprehensive tests for the task manager using Jest:
   - Unit tests for all Task class methods
   - Integration tests for file persistence
   - Edge cases like empty lists, invalid inputs
   ```

4. **Documentation**:
   ```
   Create a README.md with:
   - Project description and features
   - Installation instructions
   - Usage examples with sample output
   - API documentation for developers
   ```

5. **Git workflow**:
   ```
   Help me create a proper commit history:
   1. Commit the initial project structure
   2. Create a feature branch for "priority-levels"
   3. Add priority (low, medium, high) to tasks
   4. Create a commit message following conventional commits
   ```

### Expected Outcomes

- Build a functional application from scratch
- Experience iterative development with AI assistance
- Practice the full development cycle: concept → code → tests → docs
- Understand Gemini's file creation and modification capabilities

[← Back to Table of Contents](#table-of-contents)

---

## Lab 1: First Steps with Gemini CLI

**Duration**: 10 minutes

**Goal**: Get comfortable with the Gemini CLI interface and basic commands

### Setup

1. Navigate to any existing project directory
2. Start Gemini CLI: `gemini`
3. Familiarize yourself with the interface

### Exercises

1. **Basic interaction**:
   ```
   What are your main capabilities for helping with development?
   ```

2. **Slash commands exploration**:
   ```
   /help
   ```
   Review the available slash commands.

3. **Shell integration**:
   ```
   !ls -la
   ```
   Try executing a shell command and observe how Gemini processes the output.

4. **Memory commands**:
   ```
   /memory show
   ```
   See what context (if any) is currently loaded.

5. **Keyboard shortcuts**:
   - Try `Ctrl+L` to clear the screen
   - Try `Ctrl+Y` to toggle YOLO mode (observe the indicator change)
   - Try `Ctrl+Y` again to toggle back to default mode

### Expected Outcomes

- Understand Gemini CLI's conversational interface
- Know the essential slash commands
- Be comfortable with shell integration
- Understand YOLO mode toggle

[← Back to Table of Contents](#table-of-contents)

---

## Lab 2: Code Exploration

**Duration**: 15 minutes

**Goal**: Use Gemini CLI to understand complex codebases

### Setup

Choose one of the provided exercise projects:
- `exercises/python/weather-app` (Flask application)
- `exercises/javascript/task-manager` (Node.js CLI app)
- `exercises/java/bookstore-api` (Spring Boot REST API)

Navigate to the project directory and start Gemini CLI.

### Exercises

1. **Project overview**:
   ```
   Analyze the architecture of this project and explain the main components.
   Reference @./src/ to examine the source code.
   ```

2. **Technology identification**:
   ```
   What frameworks, libraries, and tools does this project use?
   Check @./package.json or @./pom.xml for dependencies.
   ```

3. **Entry point discovery**:
   ```
   Show me the main entry point of this application and trace the
   initialization flow.
   ```

4. **File reference practice**:
   ```
   Explain how @./src/routes.py handles incoming requests and
   what middleware is involved.
   ```
   (Adjust the file path for your chosen project)

5. **Architecture documentation**:
   ```
   Create a Mermaid diagram showing the main components and their
   relationships in this project.
   ```

6. **Web search integration**:
   ```
   Search the web for best practices for [Flask/Express/Spring Boot]
   application structure and compare with this project.
   ```

### Expected Outcomes

- Quickly understand unfamiliar codebases
- Master file references with `@` syntax
- Leverage web search for current best practices
- Generate visual documentation

[← Back to Table of Contents](#table-of-contents)

---

## Lab 3: GEMINI.md and Context Management

**Duration**: 20 minutes

**Goal**: Set up effective project context using GEMINI.md files

### Setup

Continue with the project from Lab 2, or start fresh in a new directory.

### Exercises

1. **Generate initial GEMINI.md**:
   ```
   /init
   ```
   Review the generated file and understand its structure.

2. **Customize the context**:
   ```
   Update the GEMINI.md to include:
   - Our team's coding standards (PEP 8 for Python, or equivalent)
   - Preferred testing frameworks and patterns
   - Current sprint focus: implementing caching
   - Code review checklist items
   ```

3. **Test context loading**:
   ```
   /memory show
   ```
   Verify your customizations are loaded.

4. **Create hierarchical context**:
   ```bash
   # Create subdirectory-specific context
   mkdir -p src/api
   ```

   Then ask Gemini:
   ```
   Create a GEMINI.md file for the src/api/ directory that specifies:
   - All API endpoints should return JSON
   - Use consistent error response format
   - Include request validation
   - Document all endpoints with OpenAPI comments
   ```

5. **Global context setup**:
   ```
   Help me create a global GEMINI.md at ~/.gemini/GEMINI.md with:
   - My preferred coding style (concise, well-documented)
   - Common libraries I use across projects
   - My Git commit message format preferences
   ```

6. **Modular imports**:
   ```
   Break the project GEMINI.md into modular files:
   - Create docs/coding-standards.md
   - Create docs/api-guidelines.md
   - Update GEMINI.md to import these using @docs/coding-standards.md syntax
   ```

7. **Refresh and verify**:
   ```
   /memory refresh
   /memory show
   ```
   Confirm all contexts are properly loaded.

### Expected Outcomes

- Create effective GEMINI.md files
- Understand hierarchical context loading
- Use modular imports for maintainability
- Set up global and project-specific context

[← Back to Table of Contents](#table-of-contents)

---

## Lab 4: Test Generation

**Duration**: 15 minutes

**Goal**: Generate comprehensive test suites with Gemini CLI

### Setup

Use the project from previous labs or choose a new exercise project with existing source code.

### Exercises

1. **Unit test generation**:
   ```
   Create unit tests for @./src/services/task_service.py with:
   - Tests for all public methods
   - Edge cases (empty inputs, null values)
   - Mocking of external dependencies
   Use pytest as the testing framework.
   ```
   (Adjust file path for your project)

2. **Test coverage analysis**:
   ```
   Analyze @./src/models/ and identify which classes and methods
   are missing test coverage. Generate tests to fill the gaps.
   ```

3. **Edge case discovery**:
   ```
   What edge cases should I test for the user authentication flow?
   List them and generate test cases for each.
   ```

4. **Integration tests**:
   ```
   Create integration tests for the API endpoints in @./src/routes/
   that test the full request-response cycle with test fixtures.
   ```

5. **Test data generation**:
   ```
   Generate realistic test fixtures for:
   - 10 sample users with varied data
   - 20 sample tasks with different statuses and dates
   - Edge cases like unicode characters, very long strings
   Save as JSON files in tests/fixtures/
   ```

6. **Run and verify**:
   ```bash
   # Execute the generated tests
   !pytest -v
   # Or for Node.js:
   !npm test
   ```

   Then ask:
   ```
   Analyze the test results and fix any failing tests.
   ```

### Expected Outcomes

- Generate comprehensive test suites
- Identify and test edge cases
- Create realistic test fixtures
- Iterate on failing tests

[← Back to Table of Contents](#table-of-contents)

---

## Lab 5: Configuration and Safety

**Duration**: 20 minutes

**Goal**: Configure Gemini CLI for safe, efficient workflows

### Setup

Create a test project for experimenting with configuration:
```bash
mkdir config-test && cd config-test
git init
echo "# Config Test" > README.md
```

### Exercises

1. **Explore settings**:
   ```
   /settings
   ```
   Review the current settings interface.

2. **Create project settings**:
   ```
   Create a .gemini/settings.json file with:
   - Vim mode enabled
   - Checkpointing enabled
   - Sandbox mode disabled
   - Hide tips set to true
   ```

3. **Tool restrictions**:
   ```
   Update settings.json to:
   - Exclude the shell tool for safety
   - Only allow read_file, write_file, and glob tools
   ```

4. **Test sandbox mode**:
   ```bash
   # Start in sandbox mode
   gemini --sandbox
   ```

   Then try:
   ```
   Create a file called test.txt with "Hello World"
   ```
   Observe how sandbox mode affects file operations.

5. **Checkpointing practice**:

   Enable checkpointing in settings, then:
   ```
   Create a complex file structure:
   - src/index.js with a basic Express server
   - src/routes/api.js with sample routes
   - package.json with dependencies
   ```

   Then:
   ```
   /restore list
   ```
   View available checkpoints.

6. **Approval modes**:
   ```bash
   # Try different approval modes
   gemini --approval-mode auto_edit
   ```

   Request a file edit and observe auto-approval behavior.

   ```bash
   # Compare with YOLO mode
   gemini --yolo
   ```

   Try creating files and observe the difference.

7. **Environment variables**:
   ```
   Create a .gemini/.env file with:
   GEMINI_MODEL=gemini-2.5-flash

   Then restart Gemini and verify the model change.
   ```

### Expected Outcomes

- Configure project-specific settings
- Understand sandbox and checkpointing
- Practice different approval modes
- Set up environment-based configuration

[← Back to Table of Contents](#table-of-contents)

---

## Lab 6: Advanced Features

**Duration**: 30 minutes

**Goal**: Master MCP servers, extensions, custom commands, and session management

### Part A: Session Management (5 minutes)

1. **Create a session**:
   Start an interactive session and do some work:
   ```
   gemini
   > Create a simple Python calculator module with add, subtract, multiply, divide
   > Add error handling for division by zero
   > Create tests for the calculator
   ```
   Exit with `Ctrl+D`

2. **List sessions**:
   ```bash
   gemini --list-sessions
   ```

3. **Resume session**:
   ```bash
   gemini --resume latest
   ```
   Continue where you left off:
   ```
   Add a power function to the calculator and update the tests
   ```

### Part B: Custom Commands (10 minutes)

4. **Create a review command**:
   ```bash
   mkdir -p ~/.gemini/commands
   ```

   Then ask Gemini:
   ```
   Create a custom command file at ~/.gemini/commands/review.toml that:
   - Is named "review"
   - Reviews code for security, performance, and best practices
   - Accepts a file path as input
   - Provides structured output with severity levels
   ```

5. **Test the custom command**:
   In a new session, create a file to review:
   ```
   Create a file called sample.py with some intentionally problematic code:
   - SQL injection vulnerability
   - Hardcoded credentials
   - Inefficient loop
   ```

   Then use your command to review it.

6. **Create a docs command**:
   ```
   Create a custom command at ~/.gemini/commands/docs.toml that:
   - Generates documentation for a given file or directory
   - Includes function signatures, parameters, return types
   - Creates markdown output suitable for a README
   ```

### Part C: MCP Server Integration (10 minutes)

7. **List available MCP servers**:
   ```bash
   gemini mcp list
   ```

8. **Configure GitHub MCP** (if you have a GitHub token):
   ```
   Help me configure the GitHub MCP server in .gemini/settings.json:
   - Use the @modelcontextprotocol/server-github package
   - Set up my GITHUB_TOKEN from environment
   - Include only repository and issue tools
   ```

9. **Test MCP integration**:
   If configured:
   ```
   Use the GitHub MCP to list my recent repositories
   ```

10. **Explore MCP tools**:
    ```
    What MCP tools are available in this session?
    Show me an example of using one of them.
    ```

### Part D: Output Formats (5 minutes)

11. **JSON output for scripting**:
    ```bash
    gemini -o json "List the files in current directory and describe each"
    ```

    Observe the structured output format.

12. **Stream JSON**:
    ```bash
    gemini -o stream-json "Explain the concept of microservices architecture"
    ```

    Watch the real-time streaming output.

13. **Piped workflows**:
    ```bash
    echo "What are the top 5 Python web frameworks?" | gemini -o json
    ```

### Part E: Extensions (optional, 5 minutes)

14. **List extensions**:
    ```bash
    gemini --list-extensions
    ```

15. **Create a simple extension**:
    ```
    Help me create a basic extension at ~/.gemini/extensions/my-tools/
    that adds a custom tool for formatting code.
    Include the gemini-extension.json configuration.
    ```

16. **Enable specific extensions**:
    ```bash
    gemini -e my-tools "Format the code in @./src/"
    ```

### Expected Outcomes

After completing this lab:
- Manage and resume sessions effectively
- Create reusable custom commands
- Configure and use MCP servers
- Use output formats for automation
- Understand the extension system

[← Back to Table of Contents](#table-of-contents)

---

## Tips for Success

### Effective Prompting

- **Be specific** about what you want to achieve
- **Use file references** (`@path/to/file`) for context
- **Iterate** for complex tasks - don't try everything at once
- **Provide examples** when the output format matters

### Best Practices

- Start with default approval mode, use YOLO after building trust
- Enable checkpointing before risky operations
- Keep GEMINI.md files updated with current project state
- Commit regularly to have a safety net
- Review all AI-generated code before accepting

### Common Issues and Solutions

**Issue**: Gemini doesn't understand the project structure
**Solution**: Create a comprehensive GEMINI.md with architecture details

**Issue**: Generated code doesn't match project style
**Solution**: Add coding standards to your GEMINI.md

**Issue**: API rate limits
**Solution**: Use Gemini 2.5 Flash for faster, cheaper operations

**Issue**: Context not loading
**Solution**: Run `/memory refresh` and check file paths

**Issue**: MCP server not connecting
**Solution**: Check server configuration in settings.json and test with `gemini mcp test`

---

## Next Steps

After completing these labs:

1. **Practice daily**: Use Gemini CLI for regular development tasks
2. **Customize**: Build your personal GEMINI.md and command library
3. **Explore MCP**: Set up servers for your common tools and services
4. **Share**: Document workflows for your team
5. **Stay updated**: Follow Gemini CLI releases for new features

## Additional Resources

- [Gemini CLI Documentation](https://github.com/google-gemini/gemini-cli)
- [Google AI Studio](https://aistudio.google.com/) - API keys and playground
- [MCP Server Registry](https://modelcontextprotocol.io/registry)
- [Gemini CLI Cheatsheet](https://www.philschmid.de/gemini-cli-cheatsheet)
