# React Component Creation Template

**Category**: Code Generation
**Tier**: Free
**Best For**: Creating comprehensive React components with TypeScript and best practices

## Description

Creates comprehensive React components using TypeScript with proper type definitions, hooks, error handling, accessibility considerations, and testing. This template ensures your React components follow modern best practices and include comprehensive documentation.

## Template

```
Create a React component with the following specifications:

**Component Name:** {componentName}
**Purpose:** {componentPurpose}

**Requirements:**
- Use TypeScript with proper type definitions
- Implement functional component with React hooks
- Follow React best practices and conventions
- Include proper prop validation and TypeScript interfaces
- Add comprehensive JSDoc comments
- Implement error boundaries and loading states
- Include accessibility (a11y) considerations
- Follow modern React patterns (hooks, context if needed)

**Component Structure:**
```typescript
import React, { useState, useEffect, useCallback } from 'react';

// Type definitions
interface {componentName}Props {
  // Define prop types here
  className?: string;
  children?: React.ReactNode;
}

interface {componentName}State {
  // Define internal state types
}

/**
 * {componentPurpose}
 * @param props - Component props
 * @returns JSX.Element
 */
const {componentName}: React.FC<{componentName}Props> = ({
  className = '',
  children,
  ...props
}) => {
  // State management
  const [state, setState] = useState<{componentName}State>({});
  const [loading, setLoading] = useState(false);
  const [error, setError] = useState<string | null>(null);

  // Event handlers
  const handleAction = useCallback(() => {
    // Implementation
  }, []);

  // Effects
  useEffect(() => {
    // Lifecycle logic
  }, []);

  // Render
  return (
    <div className={\`component-name \${className}\`} {...props}>
      {loading && <div>Loading...</div>}
      {error && <div role="alert">Error: {error}</div>}
      {children}
    </div>
  );
};

export default {componentName};
```

**Additional Requirements:**
- Include unit tests using React Testing Library
- Add Storybook stories for component documentation
- Implement responsive design considerations
- Include proper ARIA labels and roles
- Add CSS modules or styled-components styling
- Include prop default values and validation
- Add comprehensive error handling

**Testing Examples:**
```typescript
import { render, screen, fireEvent } from '@testing-library/react';
import {componentName} from './{componentName}';

describe('{componentName}', () => {
  it('renders correctly', () => {
    render(<{componentName} />);
    // Test assertions
  });

  it('handles user interactions', () => {
    render(<{componentName} />);
    // Interaction tests
  });
});
```

Please implement the complete component with TypeScript, tests, and documentation.
```

## Variables

- `componentName` (string): Name of the component (default: "MyComponent")
- `componentPurpose` (string): What the component does (default: "A reusable React component")

## Example Usage

### Input
```
Build a React component
```

### Optimized Output
```
Create a React component with the following specifications:

**Component Name:** UserCard
**Purpose:** A reusable card component for displaying user information

**Requirements:**
- Use TypeScript with proper type definitions
- Implement functional component with React hooks
- Follow React best practices and conventions
- Include proper prop validation and TypeScript interfaces
- Add comprehensive JSDoc comments
- Implement error boundaries and loading states
- Include accessibility (a11y) considerations
- Follow modern React patterns (hooks, context if needed)

**Component Structure:**
```typescript
import React, { useState, useEffect, useCallback } from 'react';

// Type definitions
interface UserCardProps {
  user: {
    id: string;
    name: string;
    email: string;
    avatar?: string;
  };
  className?: string;
  onClick?: () => void;
}

/**
 * A reusable card component for displaying user information
 * @param props - Component props
 * @returns JSX.Element
 */
const UserCard: React.FC<UserCardProps> = ({
  user,
  className = '',
  onClick,
  ...props
}) => {
  // Component implementation
};

export default UserCard;
```

Please implement the complete component with TypeScript, tests, and documentation.
```

## When This Template Triggers

- Phrases like "create React component", "build component", "React functional component"
- Frontend development requests
- UI component creation

## Benefits

- Ensures TypeScript integration
- Includes modern React patterns
- Provides accessibility considerations
- Includes testing framework
- Promotes component reusability
- Follows React best practices
- Includes error handling patterns