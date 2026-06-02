# Contributing to GitHub Follow Analyzer

First off, thank you for considering contributing to GitHub Follow Analyzer! 🎉

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Coding Standards](#coding-standards)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Features](#suggesting-features)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## How Can I Contribute?

### 🐛 Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates. When you create a bug report, include as many details as possible:

- **Use a clear and descriptive title**
- **Describe the exact steps to reproduce the problem**
- **Provide specific examples** (screenshots, code snippets)
- **Describe the behavior you observed** and what you expected
- **Include browser and OS information**

**Bug Report Template:**

```markdown
**Describe the bug**
A clear description of what the bug is.

**To Reproduce**
Steps to reproduce:
1. Go to '...'
2. Click on '...'
3. See error

**Expected behavior**
What you expected to happen.

**Screenshots**
If applicable, add screenshots.

**Environment:**
 - Browser: [e.g. Chrome 120]
 - OS: [e.g. Windows 11]
 - Version: [e.g. 2.0.0]
```

### ✨ Suggesting Features

Feature suggestions are welcome! Please provide:

- **Clear and descriptive title**
- **Detailed description** of the proposed feature
- **Use cases** explaining why this would be useful
- **Mockups or examples** if applicable

**Feature Request Template:**

```markdown
**Is your feature request related to a problem?**
A clear description of the problem.

**Describe the solution you'd like**
What you want to happen.

**Describe alternatives you've considered**
Other solutions you've thought about.

**Additional context**
Any other context, screenshots, or mockups.
```

## Development Setup

1. **Fork and Clone**
   ```bash
   git clone https://github.com/your-username/github-analyzer.git
   cd github-analyzer
   ```

2. **Install Dependencies** (optional, for linting/formatting)
   ```bash
   npm install
   ```

3. **Open in Browser**
   ```bash
   # Simply open index.html in your browser
   # Or use a local server:
   npm start
   ```

4. **Make Changes**
   - Edit `index.html` for the main application
   - Test thoroughly in multiple browsers
   - Ensure responsive design works

5. **Test**
   - Test with different GitHub accounts
   - Test with and without Personal Access Token
   - Test error scenarios (rate limits, invalid users)
   - Verify Excel export works correctly

## Coding Standards

### JavaScript

- Use **ES6+** features
- Use `const` and `let`, never `var`
- Use **template literals** for string interpolation
- Use **arrow functions** where appropriate
- Add **comments** for complex logic
- Keep functions **small and focused**
- Use **meaningful variable names**

**Example:**
```javascript
// Good
const fetchUserData = async (username) => {
  const response = await fetch(`https://api.github.com/users/${username}`);
  return response.json();
};

// Bad
var getData = function(u) {
  var r = fetch('https://api.github.com/users/' + u);
  return r.json();
}
```

### CSS

- Use **CSS custom properties** for colors and values
- Follow **BEM-like** naming for classes when adding new ones
- Keep styles **organized** by component
- Use **flexbox/grid** for layouts
- Ensure **responsive design**

### HTML

- Use **semantic HTML5** elements
- Add **ARIA labels** for accessibility
- Keep markup **clean and readable**
- Use **data attributes** for i18n strings

## Commit Guidelines

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, no code change)
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

### Examples

```bash
feat(export): add CSV export option
fix(ui): correct mobile responsive layout
docs(readme): update installation instructions
style(css): format code with prettier
refactor(api): simplify error handling
perf(render): optimize user list rendering
```

## Pull Request Process

1. **Create a Branch**
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/bug-description
   ```

2. **Make Your Changes**
   - Follow coding standards
   - Add comments where needed
   - Update documentation if needed

3. **Test Thoroughly**
   - Test in multiple browsers
   - Test edge cases
   - Verify no regressions

4. **Commit Your Changes**
   ```bash
   git add .
   git commit -m "feat: add amazing feature"
   ```

5. **Push to Your Fork**
   ```bash
   git push origin feature/your-feature-name
   ```

6. **Open a Pull Request**
   - Use a clear title and description
   - Reference any related issues
   - Add screenshots if UI changes
   - Wait for review

### Pull Request Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
- [ ] Tested in Chrome
- [ ] Tested in Firefox
- [ ] Tested in Safari
- [ ] Tested mobile responsive
- [ ] Tested with/without token

## Screenshots
If applicable, add screenshots

## Checklist
- [ ] Code follows project style
- [ ] Comments added for complex logic
- [ ] Documentation updated
- [ ] No console errors
- [ ] Tested thoroughly
```

## File Structure

When adding new files, follow this structure:

```
github-analyzer/
├── index.html              # Main app
├── manifest.json           # PWA manifest
├── service-worker.js       # Service worker (if added)
├── assets/
│   ├── screenshots/        # Screenshots for README
│   ├── icons/              # PWA icons
│   └── images/             # Other images
├── docs/                   # Additional documentation
├── .github/
│   ├── workflows/          # GitHub Actions
│   ├── ISSUE_TEMPLATE/     # Issue templates
│   └── PULL_REQUEST_TEMPLATE.md
├── README.md               # Turkish docs
├── README_EN.md            # English docs
├── CONTRIBUTING.md         # This file
├── CODE_OF_CONDUCT.md      # Code of conduct
├── CHANGELOG.md            # Version history
├── LICENSE                 # MIT License
└── package.json            # Project metadata
```

## Questions?

Feel free to open an issue with the `question` label if you have any questions about contributing!

## Recognition

Contributors will be recognized in:
- GitHub contributors page
- Project README (for significant contributions)
- Release notes

Thank you for contributing! 🙏
