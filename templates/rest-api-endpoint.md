# REST API Endpoint Creation Template

**Category**: Code Generation
**Tier**: Free
**Best For**: Creating comprehensive REST API endpoints with full specifications

## Description

Creates comprehensive RESTful API endpoints with proper validation, error handling, security measures, and documentation. This template ensures your API endpoints follow REST best practices and include proper status codes and authentication.

## Template

```
Create a RESTful API endpoint with the following specifications:

**Endpoint:** {method} {path}
**Purpose:** {purpose}

**Requirements:**
- Accept {requestFormat} payload with proper validation
- Implement input validation for all required fields
- Use appropriate HTTP status codes and error handling
- Include proper authentication/authorization if needed
- Add rate limiting and security measures
- Follow REST API best practices and conventions
- Include comprehensive error messages
- Add request/response examples and documentation

**Request Payload Validation:**
- Required fields: {requiredFields}
- Optional fields: {optionalFields}
- Data types and constraints for each field
- Custom validation rules

**Response Format:**
```json
{
  "success": boolean,
  "data": {
    // Response data structure
  },
  "message": "string",
  "errors": [
    // Error details if any
  ]
}
```

**HTTP Status Codes:**
- 200/201: Success responses
- 400: Bad request (validation errors)
- 401: Unauthorized
- 403: Forbidden
- 404: Not found
- 409: Conflict (duplicate resources)
- 429: Rate limit exceeded
- 500: Internal server error

**Security Considerations:**
- Input sanitization and validation
- Rate limiting implementation
- Authentication/authorization checks
- CORS configuration if needed
- SQL injection and XSS prevention

**Testing Requirements:**
- Unit tests for validation logic
- Integration tests for full endpoint flow
- Error scenario testing
- Performance testing for rate limits

Please implement the complete endpoint with middleware, validation, error handling, and comprehensive documentation.
```

## Variables

- `method` (string): HTTP method (default: "POST")
- `path` (string): API endpoint path (default: "/api/resource")
- `purpose` (string): What the endpoint does (default: "Create a new resource")
- `requestFormat` (string): Request payload format (default: "JSON")
- `requiredFields` (string): Required fields list (default: "name, email")
- `optionalFields` (string): Optional fields list (default: "description")

## Example Usage

### Input
```
Create a REST API endpoint
```

### Optimized Output
```
Create a RESTful API endpoint for user management with the following specifications:

**Endpoint:** POST /api/users
**Purpose:** Create a new user account

**Requirements:**
- Accept JSON payload with: email, password, firstName, lastName
- Validate email format and password strength (min 8 chars, 1 uppercase, 1 number)
- Hash password using bcrypt before storage
- Return 201 status with user object (excluding password)
- Handle duplicate email errors with 409 status
- Include proper error messages and status codes
- Add rate limiting (5 requests per minute per IP)

**Response Format:**
```json
{
  "success": true,
  "data": {
    "id": "uuid",
    "email": "user@example.com",
    "firstName": "John",
    "lastName": "Doe",
    "createdAt": "2024-01-01T00:00:00Z"
  }
}
```
```

## When This Template Triggers

- Phrases like "create API", "build endpoint", "REST API"
- API development requests
- Backend service creation

## Benefits

- Ensures comprehensive API documentation
- Includes proper security considerations
- Provides error handling patterns
- Follows REST conventions
- Includes testing requirements
- Promotes API consistency and reliability