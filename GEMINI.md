# Orch - Antigravity Demo Orchestration

**Repository**: [https://github.com/agylabs/orch](https://github.com/agylabs/orch)

## Project Intent

This repository serves as the orchestration hub for managing Google Antigravity demonstration repositories within the `agylabs` organization.

## Purpose

**Orch** is designed to streamline the creation, configuration, and management of demo repositories that showcase Google Antigravity's capabilities. It provides a centralized location for:

- **Repository Management**: Tools and scripts to programmatically create new demo repositories in the `agylabs` organization
- **Configuration Templates**: Standardized templates for demo projects to ensure consistency across demonstrations
- **Automation Workflows**: Automated setup and deployment processes for rapid demo environment provisioning
- **Documentation**: Best practices and guidelines for creating effective Antigravity demonstrations

## Key Capabilities

### Current
- Project structure and intent documentation
- Foundation for repository orchestration tooling

### Planned
- **Automated Repository Creation**: Scripts leveraging GitHub APIs to create and configure new demo repositories
- **Template System**: Pre-configured project templates for common Antigravity use cases
- **Demo Lifecycle Management**: Tools for setting up, updating, and archiving demonstration repositories
- **Integration Workflows**: CI/CD pipelines and deployment automation for demo environments
- **Inventory Management**: Tracking and cataloging all active demonstration repositories

## Target Audience

This repository is intended for:
- Google Antigravity team members creating demonstrations
- Product managers showcasing Antigravity capabilities
- Engineers building proof-of-concept applications
- Anyone needing to quickly spin up Antigravity demo environments

## Getting Started

*(To be expanded as tooling is developed)*

1. Clone this repository
2. Review available templates and scripts
3. Use the orchestration tools to create new demo repositories
4. Follow the configuration guidelines for your specific demo needs

## Workflow

To maintain a clean and stable codebase, all contributors must follow this workflow:

1.  **Never push directly to `main`**: All changes must be developed in a feature or bugfix branch.
2.  **Branch Naming**: Use descriptive branch names (e.g., `feature/add-template`, `fix/api-auth`).
3.  **Frequent Commits**: Make small, logical, and frequent commits. This makes it easier to track changes and roll back if necessary.
4.  **Descriptive Commit Messages**: Write clear, concise commit messages that explain *why* a change was made.
5.  **Pull Requests**: Submit a Pull Request (PR) when your changes are ready. PRs should be reviewed and pass CI before merging into `main`.
6.  **Stay Updated**: Frequently pull the latest changes from `main` into your feature branch to resolve conflicts early.
7.  **Atomic Changes**: Each branch and PR should focus on a single task or feature.

## Repository Structure

```
orch/
├── GEMINI.md           # This file - project intent and overview
├── templates/          # (Planned) Demo project templates
├── scripts/            # (Planned) Automation scripts
└── docs/               # (Planned) Additional documentation
```

## GitHub MCP Server

This repository uses the **`github-agylabs-mcp`** MCP server for all GitHub operations. This server is pre-configured with the necessary permissions to create and manage repositories in the `agylabs` organization.

### Creating New Demo Repositories

Use the MCP server to programmatically create new demo repositories:

```javascript
mcp_github-agylabs-mcp_create_repository({
  name: "demo-repository-name",
  organization: "agylabs",
  description: "Description of your Antigravity demo",
  private: false,
  autoInit: true  // Creates with README
})
```

### Available MCP Operations

The `github-agylabs-mcp` server provides full GitHub functionality including:
- **Repository Management**: Create, update, and delete repositories
- **Content Management**: Create, update, and delete files
- **Branch Operations**: Create and manage branches
- **Pull Requests**: Create, update, and merge pull requests
- **Issues**: Create and manage issues
- **Search**: Search repositories, code, issues, and pull requests

### Best Practices

- **Always use `github-agylabs-mcp`** for GitHub operations in this project
- **Use descriptive names** for demo repositories (e.g., `antigravity-demo-auth`, `antigravity-demo-ml`)
- **Include clear descriptions** to help others understand the demo's purpose
- **Initialize with README** when creating new repositories for better documentation

## Contributing

This is an internal orchestration repository. Contributions should focus on:
- Improving automation capabilities
- Adding new demo templates
- Enhancing documentation
- Streamlining the demo creation workflow

---

*This repository is part of the Google Antigravity demonstration ecosystem.*
