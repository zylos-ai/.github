# Contributing to Zylos

Thank you for your interest in contributing to Zylos! This guide applies to all repositories in the zylos-ai organization.

## Getting Started

1. **Fork** the repository
2. **Clone** your fork locally
3. **Create a branch** from `main` for your changes
4. **Make your changes** following the guidelines below
5. **Submit a Pull Request** back to the original repository

## Development Environment

- **Node.js**: 20.0.0 or later
- **Module system**: ES Modules only (no CommonJS)
- **Package manager**: npm

## Code Standards

### ES Modules

All code uses ES Modules. Use `import`/`export`, not `require`/`module.exports`.

```javascript
// Good
import { readFile } from 'node:fs/promises';
export function myFunction() { }

// Bad
const { readFile } = require('fs/promises');
module.exports = { myFunction };
```

### Commit Messages

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <description>

[optional body]
```

Types:
- `feat`: New feature
- `fix`: Bug fix
- `chore`: Maintenance (dependencies, config, etc.)
- `docs`: Documentation changes
- `refactor`: Code changes that neither fix bugs nor add features
- `test`: Adding or updating tests

Examples:
```
feat(bot): add group chat support
fix(proxy): handle connection timeout gracefully
chore: update dependencies
docs: improve getting started guide
```

### Code Style

- Use meaningful variable and function names
- Keep functions focused and small
- Add comments only where the logic isn't self-evident
- Handle errors appropriately — don't silently swallow them

## Pull Request Process

1. **Keep PRs focused** — one feature or fix per PR
2. **Update documentation** if your changes affect user-facing behavior
3. **Update CHANGELOG.md** following [Keep a Changelog](https://keepachangelog.com/) format
4. **Test your changes** — run existing tests and add new ones where applicable
5. **Fill out the PR template** — describe what changed and why

## Component Development

To create a new Zylos component, see the [component template](https://github.com/zylos-ai/zylos-component-template). It includes lifecycle hooks, messaging scripts, PM2 integration, and an AI development guide.

## Reporting Issues

- Use the repository's issue templates for bug reports and feature requests
- Search existing issues before creating a new one
- Provide reproduction steps for bugs

## Questions?

Open a [discussion](https://github.com/orgs/zylos-ai/discussions) or file an issue in the relevant repository.
