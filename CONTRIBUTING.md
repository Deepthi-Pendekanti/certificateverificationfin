# Contributing to Student Certificate Verification System

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to this project.

## Code of Conduct

Please be respectful and constructive in all interactions with other contributors and maintainers.

## How to Contribute

### Reporting Bugs

Before creating bug reports, please check the issue list as you might find out that you don't need to create one. When you are creating a bug report, please include as many details as possible:

* **Use a clear and descriptive title**
* **Describe the exact steps which reproduce the problem**
* **Provide specific examples to demonstrate the steps**
* **Describe the behavior you observed after following the steps**
* **Explain which behavior you expected to see instead and why**
* **Include screenshots and animated GIFs if possible**
* **Include your environment details** (OS, Node.js version, etc.)

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, please include:

* **Use a clear and descriptive title**
* **Provide a step-by-step description of the suggested enhancement**
* **Provide specific examples to demonstrate the steps**
* **Describe the current behavior and expected behavior**
* **Explain why this enhancement would be useful**

### Pull Requests

* Follow the JavaScript/Solidity styleguides
* Include appropriate test cases
* End all files with a newline
* Avoid platform-dependent code

## Development Setup

1. Fork the repository
2. Clone your fork: `git clone https://github.com/your-username/student-certificate-verification.git`
3. Create a new branch: `git checkout -b feature/your-feature-name`
4. Install dependencies: `npm install`
5. Make your changes
6. Test your changes
7. Commit with clear messages: `git commit -m "Add feature description"`
8. Push to your fork: `git push origin feature/your-feature-name`
9. Submit a Pull Request

## Styleguides

### JavaScript
* Use 2-space indentation
* Use meaningful variable names
* Add comments for complex logic
* Follow ES6+ standards

### Solidity
* Use 2-space indentation
* Follow Solidity naming conventions
* Add NatSpec comments for functions
* Use SafeMath practices

## Commit Messages

* Use the present tense ("Add feature" not "Added feature")
* Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
* Limit the first line to 72 characters or less
* Reference issues and pull requests liberally after the first line

## Testing

Before submitting a pull request, please test your changes:

```bash
npm run compile
npm run migrate
npm start
```

## License

By contributing to this project, you agree that your contributions will be licensed under the ISC License.

## Questions?

Feel free to open an issue with the question tag for any clarifications needed.

Thank you for contributing!
