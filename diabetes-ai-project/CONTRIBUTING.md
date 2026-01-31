# Contributing to AI Diabetes Risk Intelligence System

First off, thank you for considering contributing to this project! 🎉

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Coding Standards](#coding-standards)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)

## Code of Conduct

This project and everyone participating in it is governed by our commitment to creating a welcoming and inclusive environment. By participating, you are expected to uphold this standard.

### Our Standards

- Using welcoming and inclusive language
- Being respectful of differing viewpoints
- Gracefully accepting constructive criticism
- Focusing on what is best for the community
- Showing empathy towards other community members

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates.

**When submitting a bug report, include**:
- A clear and descriptive title
- Steps to reproduce the behavior
- Expected behavior vs actual behavior
- Screenshots if applicable
- Browser and OS information
- Any error messages from the console

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues.

**When suggesting an enhancement, include**:
- A clear and descriptive title
- A detailed description of the proposed functionality
- Explain why this enhancement would be useful
- Provide examples of how it would work

### Code Contributions

#### Good First Issues

Look for issues labeled `good first issue` - these are great for newcomers!

#### Areas to Contribute

1. **UI/UX Improvements**
   - Design enhancements
   - Accessibility improvements
   - Responsive design fixes

2. **Data Visualization**
   - New chart types
   - Interactive features
   - Animation improvements

3. **Machine Learning**
   - Model accuracy improvements
   - Additional algorithms
   - Feature engineering

4. **Documentation**
   - README improvements
   - Code comments
   - User guides

5. **Testing**
   - Unit tests
   - Integration tests
   - Cross-browser testing

## Development Setup

### Prerequisites

- Git
- A modern web browser
- A code editor (VS Code recommended)

### Setting Up Your Development Environment

1. **Fork the repository** on GitHub

2. **Clone your fork**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/diabetes-ai-system.git
   cd diabetes-ai-system
   ```

3. **Add upstream remote**:
   ```bash
   git remote add upstream https://github.com/ORIGINAL_OWNER/diabetes-ai-system.git
   ```

4. **Create a branch**:
   ```bash
   git checkout -b feature/your-feature-name
   ```

5. **Open the project**:
   - Simply open `index.html` in your browser
   - Or use a local server for better development experience

### Development Workflow

1. Make your changes
2. Test thoroughly in multiple browsers
3. Commit your changes (see commit guidelines below)
4. Push to your fork
5. Submit a pull request

## Coding Standards

### HTML

- Use semantic HTML5 elements
- Maintain proper indentation (2 spaces)
- Include ARIA labels for accessibility
- Keep structure clean and organized

```html
<!-- Good -->
<section class="card" role="region" aria-label="Patient Input Form">
  <h2>Patient Parameters</h2>
  <!-- content -->
</section>

<!-- Avoid -->
<div class="card">
  <div class="title">Patient Parameters</div>
  <!-- content -->
</div>
```

### CSS

- Use CSS custom properties for theming
- Follow BEM naming convention where appropriate
- Keep selectors specific but not overly complex
- Group related properties together
- Comment complex calculations

```css
/* Good */
:root {
  --primary: #0A4D68;
  --accent: #05C3DD;
}

.card {
  background: var(--bg-card);
  padding: 2rem;
}

/* Avoid */
.card {
  background: rgba(17, 24, 39, 0.6);
  padding: 32px;
}
```

### JavaScript

- Use ES6+ features
- Write descriptive variable and function names
- Add comments for complex logic
- Keep functions focused and small
- Use `const` and `let`, avoid `var`
- Handle errors appropriately

```javascript
// Good
function calculateRiskScore(features) {
  const normalizedGlucose = features.glucose / 200;
  let score = 0;
  
  // Glucose is the most important factor (35%)
  score += normalizedGlucose * 35;
  
  return Math.min(score, 100);
}

// Avoid
function calc(f) {
  var g = f.glucose / 200;
  var s = 0;
  s += g * 35;
  return s > 100 ? 100 : s;
}
```

### Code Organization

- Group related functions together
- Use meaningful section comments
- Keep global variables to a minimum
- Separate concerns (UI, data processing, calculations)

```javascript
// ============================================
// ML Prediction Functions
// ============================================

function predictDiabetes(features) {
  // ...
}

function calculateFeatureImportance(features) {
  // ...
}

// ============================================
// UI Update Functions
// ============================================

function updateRiskDisplay(prediction) {
  // ...
}
```

## Commit Guidelines

### Commit Message Format

Follow the conventional commits specification:

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc)
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Adding tests
- `chore`: Maintenance tasks

### Examples

```bash
feat(ui): add dark mode toggle button

Added a toggle button in the header to switch between light and dark themes.
The preference is saved in localStorage for persistence.

Closes #123
```

```bash
fix(predictions): correct BMI normalization calculation

The BMI was being normalized incorrectly, leading to inflated risk scores.
Fixed the maximum value from 50 to 67.1 based on the dataset.

Fixes #456
```

```bash
docs(readme): add installation instructions for Windows

Added specific instructions for Windows users to run the application
using different methods.
```

## Pull Request Process

### Before Submitting

1. **Test your changes**:
   - Test in multiple browsers (Chrome, Firefox, Safari)
   - Test responsive design on different screen sizes
   - Check console for errors
   - Verify all features still work

2. **Update documentation**:
   - Update README if needed
   - Add comments to complex code
   - Update relevant documentation files

3. **Follow coding standards**:
   - Run code through a formatter
   - Ensure consistent style
   - Remove console.logs and debug code

### Submitting the Pull Request

1. **Write a clear title**:
   ```
   feat: Add export to CSV functionality
   ```

2. **Provide detailed description**:
   - What does this PR do?
   - Why is this change needed?
   - How does it work?
   - Screenshots (if UI changes)
   - Related issues

3. **Fill out the PR template** (if available)

4. **Link related issues**:
   ```
   Closes #123
   Related to #456
   ```

### After Submitting

- Be responsive to feedback
- Make requested changes promptly
- Keep the discussion professional and constructive
- Squash commits if requested

### Review Process

1. Automated checks (if any) must pass
2. At least one maintainer approval required
3. No unresolved conversations
4. Up-to-date with main branch

## Questions?

Don't hesitate to ask questions! You can:

- Open an issue with the `question` label
- Comment on existing issues
- Reach out to the maintainers

## Recognition

All contributors will be recognized in the project! Your contributions, big or small, are valued.

---

Thank you for contributing! 🚀
