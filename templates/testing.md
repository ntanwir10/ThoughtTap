# Test Generation Template

**Category**: Testing
**Tier**: Free
**Best For**: Creating comprehensive tests

## Description

Creates comprehensive tests including unit tests, integration tests, edge cases, and realistic test data. This template ensures thorough test coverage using appropriate testing frameworks and follows testing best practices.

## Template

```
You are an expert {language} developer and testing specialist.

Create comprehensive tests for:

{input}

Generate tests that include:

1. **Unit Tests**: Test individual functions/methods
2. **Integration Tests**: Test component interactions
3. **Edge Cases**: Handle boundary conditions and errors
4. **Test Data**: Realistic test scenarios and data
5. **Assertions**: Clear expectations and validations

Use appropriate {language} testing frameworks and follow testing best practices.
Include setup, teardown, and mock data as needed.
```

## Variables

- `language` (string): Programming language for tests (automatically detected from context)

## Example Usage

### Input
```
write tests for this function
```

### Optimized Output
```
You are an expert JavaScript developer and testing specialist.

Create comprehensive tests for:

[Your function here]

Generate tests that include:

1. **Unit Tests**: Test individual functions/methods
   - Test each function in isolation
   - Verify correct return values
   - Test function behavior with various inputs
   - Validate parameter handling

2. **Integration Tests**: Test component interactions
   - Test function interactions with dependencies
   - Verify data flow between components
   - Test API integrations and external services
   - Validate system behavior end-to-end

3. **Edge Cases**: Handle boundary conditions and errors
   - Test with null/undefined inputs
   - Test with empty arrays/objects
   - Test with extremely large/small values
   - Test error conditions and exception handling
   - Test invalid input types

4. **Test Data**: Realistic test scenarios and data
   - Create representative test datasets
   - Use realistic user input patterns
   - Include both valid and invalid data
   - Test with production-like data volumes

5. **Assertions**: Clear expectations and validations
   - Use descriptive test names
   - Clear assertion messages
   - Test both positive and negative cases
   - Verify state changes and side effects

**Testing Framework Setup:**
```javascript
// Using Jest and React Testing Library (if applicable)
import { render, screen, fireEvent, waitFor } from '@testing-library/react';
import { jest } from '@jest/globals';

describe('FunctionName', () => {
  beforeEach(() => {
    // Setup before each test
  });

  afterEach(() => {
    // Cleanup after each test
    jest.clearAllMocks();
  });

  // Test cases here
});
```

**Mock Setup:**
Include proper mocking for external dependencies, API calls, and browser APIs.

Use appropriate JavaScript testing frameworks (Jest, Mocha, Jasmine) and follow testing best practices including proper test organization, descriptive naming, and comprehensive coverage.
```

## When This Template Triggers

- Phrases like "test", "testing", "unit test", "integration test"
- Requests for creating test suites
- Quality assurance requirements

## Benefits

- Ensures comprehensive test coverage
- Includes multiple testing levels
- Provides realistic test scenarios
- Uses appropriate testing frameworks
- Includes setup and teardown procedures
- Promotes testing best practices
- Language-specific testing patterns