# 🤝 Contributing to Showcase Projects

Thank you for your interest in contributing to this showcase repository! This document provides guidelines and instructions for contributing.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Development Workflow](#development-workflow)
- [Pull Request Process](#pull-request-process)
- [Coding Standards](#coding-standards)
- [Documentation](#documentation)

---

## 📜 Code of Conduct

This project follows a standard code of conduct:

- **Be respectful** - Treat everyone with respect and kindness
- **Be collaborative** - Work together and help each other
- **Be inclusive** - Welcome people of all backgrounds
- **Be professional** - Maintain professional communication

---

## 🚀 Getting Started

### Prerequisites

Before contributing, ensure you have:

- Git installed and configured
- Docker and Docker Compose (for testing projects)
- Relevant development tools for the project you're working on (JDK, Python, etc.)

### Fork and Clone

1. Fork the repository on GitHub
2. Clone your fork locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/showcase-projects.git
   cd showcase-projects
   ```
3. Add the upstream repository:
   ```bash
   git remote add upstream https://github.com/tazzledazzle/showcase-projects.git
   ```

---

## 💡 How to Contribute

### Types of Contributions

We welcome various types of contributions:

- 🐛 **Bug Fixes** - Fix issues in existing projects
- ✨ **Feature Additions** - Add new features to existing projects
- 📚 **Documentation** - Improve or add documentation
- 🎨 **Code Quality** - Refactoring and code improvements
- 🧪 **Tests** - Add or improve test coverage
- 🆕 **New Projects** - Propose and add new showcase projects

### Reporting Issues

When reporting issues:

1. Check if the issue already exists
2. Use a clear and descriptive title
3. Provide detailed information:
   - Steps to reproduce
   - Expected behavior
   - Actual behavior
   - Environment details (OS, versions, etc.)
4. Include code samples or error messages when relevant

---

## 🔄 Development Workflow

### 1. Create a Branch

Create a feature branch from `main`:

```bash
git checkout -b feature/your-feature-name
```

Use descriptive branch names:
- `feature/` - New features
- `bugfix/` - Bug fixes
- `docs/` - Documentation changes
- `refactor/` - Code refactoring

### 2. Make Changes

- Make your changes in the appropriate project directory
- Keep changes focused and atomic
- Write clear, concise commit messages
- Test your changes thoroughly

### 3. Commit Your Changes

Write meaningful commit messages:

```bash
git add .
git commit -m "Add feature: brief description of what changed"
```

**Good commit message format:**
```
<type>: <subject>

<body (optional)>

<footer (optional)>
```

Examples:
- `feat: add health check endpoint to REST API`
- `fix: correct OTel span propagation in worker`
- `docs: update installation instructions for macOS`
- `refactor: simplify job queue processing logic`

### 4. Keep Your Fork Updated

Regularly sync with upstream:

```bash
git fetch upstream
git rebase upstream/main
```

---

## 🔍 Pull Request Process

### Before Submitting

1. ✅ **Test your changes** - Ensure all tests pass
2. ✅ **Update documentation** - Update READMEs if needed
3. ✅ **Follow coding standards** - See below
4. ✅ **Run linters** - If applicable to the project
5. ✅ **Check for conflicts** - Rebase if needed

### Submitting a Pull Request

1. Push your branch to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```

2. Open a Pull Request on GitHub:
   - Use a clear, descriptive title
   - Reference any related issues
   - Provide a detailed description of changes
   - Explain why the change is needed
   - Include screenshots for UI changes

3. **PR Template:**
   ```markdown
   ## Description
   Brief description of changes

   ## Type of Change
   - [ ] Bug fix
   - [ ] New feature
   - [ ] Documentation update
   - [ ] Refactoring
   - [ ] Other (specify)

   ## Testing
   Describe how you tested your changes

   ## Checklist
   - [ ] Code follows project style
   - [ ] Tests added/updated
   - [ ] Documentation updated
   - [ ] All tests pass
   ```

### Review Process

- Maintainers will review your PR
- Address any feedback or requested changes
- Once approved, your PR will be merged

---

## 💻 Coding Standards

### General Principles

- **Clarity** - Write clear, readable code
- **Consistency** - Follow existing code style
- **Simplicity** - Keep it simple and maintainable
- **Documentation** - Comment complex logic

### Project-Specific Standards

#### Python Projects (FastAPI, Worker)
- Follow PEP 8 style guide
- Use type hints where applicable
- Write docstrings for functions and classes
- Format with `black` (if configured)
- Lint with `flake8` or `pylint` (if configured)

#### Java/Kotlin Projects (JVM Build)
- Follow Kotlin coding conventions
- Use meaningful variable names
- Write unit tests with JUnit
- Use Gradle for dependency management

#### Docker
- Use multi-stage builds when appropriate
- Minimize image layers
- Don't include sensitive data
- Use specific version tags, not `latest`

### Markdown Standards

- Use ATX-style headers (`#` syntax)
- Include blank lines around headers and code blocks
- Use tables for structured data
- Add emojis sparingly for visual enhancement
- Keep line length reasonable (~100 chars)

---

## 📖 Documentation

### Documentation Standards

- Keep README files up to date
- Include setup instructions
- Provide usage examples
- Document API endpoints
- Add architecture diagrams when helpful
- Explain design decisions in docs/

### Adding a New Project

When adding a new showcase project:

1. Create a new directory with a descriptive name
2. Include a comprehensive README.md:
   - Project overview and problem/solution
   - Architecture description
   - Setup and installation
   - Usage examples
   - Testing instructions
   - License information
3. Add the project to the root README.md
4. Include relevant documentation in a `docs/` subdirectory
5. Add a `docker-compose.yml` if applicable
6. Include tests (if applicable)

---

## 🎯 Quality Checklist

Before submitting your contribution, ensure:

- ✅ Code builds without errors
- ✅ All tests pass
- ✅ New features have tests
- ✅ Documentation is updated
- ✅ Code follows project style
- ✅ Commit messages are clear
- ✅ No sensitive data included
- ✅ Docker images build successfully (if applicable)
- ✅ README is accurate and complete

---

## 🆘 Getting Help

If you need help or have questions:

1. Check existing documentation
2. Search for similar issues
3. Open a GitHub issue for discussion
4. Tag maintainers if needed

---

## 📝 License

By contributing to this project, you agree that your contributions will be licensed under the MIT License.

---

## 🙏 Thank You!

Your contributions help make this showcase repository better for everyone. We appreciate your time and effort!

---

[← Back to README](./README.md)
