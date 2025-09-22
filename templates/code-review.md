# Code Review Template

**Category**: Review
**Tier**: Free
**Best For**: Providing comprehensive code review with feedback

## Description

Provides comprehensive code review covering code quality, best practices, performance, security, and testing. This template ensures thorough analysis of code with constructive and specific feedback for improvement.

## Template

```
You are an expert {language} developer and code reviewer.

Please review the following code:

{input}

Provide a comprehensive code review covering:

1. **Code Quality**: Readability, maintainability, and style
2. **Best Practices**: Adherence to {language} conventions
3. **Performance**: Potential optimizations and bottlenecks
4. **Security**: Security considerations and vulnerabilities
5. **Testing**: Testability and test coverage suggestions
6. **Recommendations**: Specific improvements with code examples

Be constructive and specific in your feedback.
```

## Variables

- `language` (string): Programming language being reviewed (automatically detected from context)

## Example Usage

### Input
```
review this JavaScript code
```

### Optimized Output
```
You are an expert JavaScript developer and code reviewer.

Please review the following code:

[Your code here]

Provide a comprehensive code review covering:

1. **Code Quality**: Readability, maintainability, and style
   - Variable naming conventions
   - Function structure and organization
   - Code formatting and consistency
   - Documentation and comments

2. **Best Practices**: Adherence to JavaScript conventions
   - ES6+ modern syntax usage
   - Proper error handling
   - Function composition and modularity
   - Async/await patterns

3. **Performance**: Potential optimizations and bottlenecks
   - Algorithm efficiency
   - Memory usage considerations
   - Loop optimizations
   - DOM manipulation efficiency (if applicable)

4. **Security**: Security considerations and vulnerabilities
   - Input validation and sanitization
   - XSS and injection prevention
   - Authentication and authorization
   - Data exposure risks

5. **Testing**: Testability and test coverage suggestions
   - Unit test opportunities
   - Test structure recommendations
   - Mock and stub strategies
   - Edge case coverage

6. **Recommendations**: Specific improvements with code examples
   - Refactoring suggestions
   - Alternative approaches
   - Library/framework recommendations
   - Code examples for improvements

Be constructive and specific in your feedback, providing actionable suggestions for improvement.
```

## When This Template Triggers

- Phrases like "review code", "check code", "evaluate implementation"
- Code quality assessment requests
- Feedback requests on existing code

## Benefits

- Provides structured code review framework
- Covers multiple quality dimensions
- Ensures comprehensive analysis
- Promotes best practices
- Includes security considerations
- Suggests specific improvements
- Language-aware feedback