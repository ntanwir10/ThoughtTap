# Code Refactoring Template

**Category**: Refactoring
**Tier**: Free
**Best For**: Improving code structure and quality

## Description

Improves code structure and quality while maintaining existing functionality. This template provides a systematic approach to refactoring with clear explanations of changes, benefits, and testing strategies.

## Template

```
You are an expert {language} developer specializing in code refactoring.

Please refactor the following code:

{input}

Refactoring goals:
- Improve code readability and maintainability
- Apply {language} best practices and patterns
- Reduce code duplication and complexity
- Enhance performance where possible
- Maintain existing functionality

Provide:
1. **Refactored Code**: The improved version
2. **Explanation**: What changes were made and why
3. **Benefits**: How the refactoring improves the code
4. **Testing**: How to verify functionality is preserved
```

## Variables

- `language` (string): Programming language being refactored (automatically detected from context)

## Example Usage

### Input
```
refactor this messy code
```

### Optimized Output
```
You are an expert JavaScript developer specializing in code refactoring.

Please refactor the following code:

[Your code here]

Refactoring goals:
- Improve code readability and maintainability
- Apply JavaScript best practices and patterns
- Reduce code duplication and complexity
- Enhance performance where possible
- Maintain existing functionality

Provide:

1. **Refactored Code**: The improved version
   - Use modern ES6+ syntax and features
   - Apply proper function composition
   - Implement consistent naming conventions
   - Organize code into logical modules
   - Add proper error handling

2. **Explanation**: What changes were made and why
   - Detailed breakdown of each improvement
   - Reasoning behind architectural decisions
   - Best practices applied
   - Pattern implementations used

3. **Benefits**: How the refactoring improves the code
   - Improved readability and maintainability
   - Better performance characteristics
   - Reduced complexity and coupling
   - Enhanced testability
   - Future extensibility improvements

4. **Testing**: How to verify functionality is preserved
   - Unit test recommendations
   - Integration testing approach
   - Behavior verification strategies
   - Performance benchmarking suggestions
   - Regression testing checklist

Include comments explaining the refactoring decisions and maintain backward compatibility where possible.
```

## When This Template Triggers

- Phrases like "refactor", "improve", "optimize", "clean up", "restructure"
- Code improvement requests
- Legacy code modernization

## Benefits

- Maintains functionality while improving structure
- Provides clear explanation of changes
- Includes testing verification strategies
- Applies language-specific best practices
- Reduces technical debt
- Improves code maintainability
- Enhances performance where applicable