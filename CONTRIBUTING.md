# Contributing to Benjamin Fin Space App

Thank you for your interest in contributing to Benjamin! We welcome all contributions, big or small.

## Ways to Contribute

### 1. Code Contributions

- Fix bugs
- Implement new features
- Improve performance
- Add tests

### 2. Documentation

- Improve existing documentation
- Fix typos
- Add examples
- Translate documentation

### 3. Models and Strategies

- Add new quantitative models
- Contribute trading strategies
- Share research findings

### 4. Community

- Answer questions in issues
- Share your experience
- Help others

## Development Setup

### 1. Fork and Clone

```bash
git clone https://github.com/Soros2040/benjamin-fin-space-app.git
cd benjamin-fin-space-app/benjamin
```

### 2. Setup BenQ Engine

```bash
cd engines/benq
pip install -e .[dev]
```

### 3. Setup Alex Engine (Dify)

```bash
cd engines/alex/dify
# Follow https://docs.dify.ai/getting-started/install-self-hosted/local-source-code
```

### 4. Setup Mobile App

```bash
cd apps/mobile
../../flutter/bin/flutter pub get
```

## Pull Request Process

1. **Create a branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes**
   - Follow the existing code style
   - Write tests for new features
   - Update documentation

3. **Commit your changes**
   - Use clear, descriptive commit messages
   - Reference issues when applicable
   ```bash
   git commit -m "Add feature X. Closes #123"
   ```

4. **Push and create PR**
   ```bash
   git push origin feature/your-feature-name
   ```

5. **Submit Pull Request**
   - Use the PR template
   - Describe your changes clearly
   - Link related issues

## Code Style

### Python

- Follow PEP 8
- Use type hints when possible
- Write docstrings for public APIs
- Add unit tests

### Dart/Flutter

- Follow Effective Dart
- Use const constructors when possible
- Add widget tests

## Testing

### BenQ Engine

```bash
cd engines/benq
pytest tests/
```

### Mobile App

```bash
cd apps/mobile
../../flutter/bin/flutter test
```

## Questions?

Feel free to ask questions in:
- GitHub Issues
- GitHub Discussions
- Discord community

## Code of Conduct

Please note that this project is released with a Contributor Code of Conduct. By participating in this project you agree to abide by its terms.

## License

By contributing, you agree that your contributions will be licensed under the project's license.
