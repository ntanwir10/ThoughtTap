# JavaScript Function Generation Template

**Category**: Code Generation
**Tier**: Free
**Best For**: Creating comprehensive JavaScript functions with full specifications

## Description

Creates comprehensive JavaScript functions with input validation, error handling, documentation, and examples. This template ensures your functions follow modern JavaScript best practices and include proper testing examples.

## Template

```
Write a JavaScript function called {functionName} that:
- Takes {parameters} as input parameter(s)
- Handles edge cases (empty inputs, null values, invalid types)
- Uses an efficient algorithm with optimal time complexity
- Returns {returnType} in the specified format
- Includes comprehensive JSDoc comments explaining the function
- Follows modern JavaScript best practices (ES6+)
- Provides usage examples and expected outputs

**Requirements:**
- Input validation with descriptive error messages
- Pure function design (no side effects)
- Comprehensive error handling
- Clear variable naming and code structure
- Include at least 3 test examples

**Example Structure:**
```javascript
/**
 * {functionDescription}
 * @param {string} paramName - Description of parameter
 * @returns {string} Description of return value
 * @throws {Error} When invalid input is provided
 */
function {functionName}(parameters) {
  // Input validation
  if (!parameter || typeof parameter !== 'expected_type') {
    throw new Error('Invalid input: parameter must be...');
  }

  // Implementation here

  return result;
}

// Usage Examples:
console.log({functionName}(validInput)); // Expected output
console.log({functionName}(edgeCase)); // Expected edge case output
```

Please implement this complete function with full documentation and examples.
```

## Variables

- `functionName` (string): Name of the function to create (default: "processData")
- `parameters` (string): Input parameters description (default: "data")
- `returnType` (string): Expected return type (default: "processed result")
- `functionDescription` (string): Brief description of what the function does

## Example Usage

### Input
```
Write a function to sort an array
```

### Optimized Output
```
Write a JavaScript function called sortArray that:
- Takes an array of numbers as input parameter
- Handles edge cases (empty arrays, single elements)
- Uses an efficient sorting algorithm (O(n log n) average case)
- Returns a new sorted array in ascending order
- Includes comprehensive JSDoc comments explaining the function
- Follows modern JavaScript best practices (ES6+)
- Provides usage examples and expected outputs

**Requirements:**
- Input validation with descriptive error messages
- Pure function design (no side effects)
- Comprehensive error handling
- Clear variable naming and code structure
- Include at least 3 test examples

Please implement this complete function with full documentation and examples.
```

## When This Template Triggers

- Phrases like "write function", "create function", "generate function"
- JavaScript-specific function requests
- General function implementation requests

## Benefits

- Ensures comprehensive function documentation
- Includes proper error handling patterns
- Provides testing examples
- Follows modern JavaScript conventions
- Promotes code reusability and maintainability