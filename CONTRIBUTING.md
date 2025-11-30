# Contributing to Eco-Route

Thank you for your interest in contributing to Eco-Route! We welcome contributions from everyone. This document provides guidelines and instructions for contributing.

## Getting Started

1. Fork the repository on GitHub
2. Clone your fork locally:
   ```bash
   git clone https://github.com/your-username/Eco-Route.git
   cd Eco-Route
   ```
3. Create a virtual environment:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate  # Windows
   source .venv/bin/activate  # macOS/Linux
   ```
4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Making Changes

1. Create a new branch for your feature:
   ```bash
   git checkout -b feature/your-feature-name
   ```
2. Make your changes and test them thoroughly
3. Commit with clear, descriptive messages:
   ```bash
   git commit -m "Add: Brief description of changes"
   ```
4. Push to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a Pull Request on GitHub

## Commit Message Guidelines

- Use clear, descriptive commit messages
- Start with a verb: Add, Fix, Update, Refactor, Docs, etc.
- Example: `Add: Real-time AQI streaming for dashboard`

## Code Style

- Follow PEP 8 Python style guidelines
- Use meaningful variable and function names
- Add comments for complex logic
- Keep functions focused and modular

## Testing

- Test your changes locally before submitting
- Ensure the Flask app runs without errors
- Test API endpoints with proper parameters
- Verify database operations work correctly

## Bug Reports

When reporting bugs, please include:
- Description of the issue
- Steps to reproduce
- Expected behavior
- Actual behavior
- Environment details (OS, Python version, etc.)

## Feature Requests

- Clearly describe the feature
- Explain the use case
- Provide examples if applicable

## Types of Contributions We Accept

- Bug fixes
- New features
- Documentation improvements
- Performance optimizations
- Code refactoring
- Test coverage improvements
- Translation improvements

## Areas for Improvement

- Frontend UI/UX enhancements
- Additional zone coverage
- Mobile app development
- API optimizations
- Database query optimization
- Caching mechanisms
- More comprehensive testing

## Questions?

Feel free to open an issue for questions or discussions about the project.

---

**Thank you for contributing to make Eco-Route better!** 🌍♻️
