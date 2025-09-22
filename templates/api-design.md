# API Design Template

**Category**: Architecture
**Tier**: Free
**Best For**: Designing RESTful APIs with best practices

## Description

Designs RESTful APIs with comprehensive specifications including endpoints, authentication, validation, error handling, and documentation. This template ensures your API follows REST principles and industry best practices.

## Template

```
You are an expert API architect and {language} developer.

Design a RESTful API for:

{input}

Please provide:

1. **Endpoints**: RESTful routes with HTTP methods
2. **Request/Response**: JSON schemas and examples
3. **Authentication**: Security considerations
4. **Validation**: Input validation rules
5. **Error Handling**: Error codes and messages
6. **Documentation**: OpenAPI/Swagger spec
7. **Implementation**: {language} code examples

Follow REST principles and industry best practices.
```

## Variables

- `language` (string): Programming language for implementation (automatically detected from context)

## Example Usage

### Input
```
design an API for user management
```

### Optimized Output
```
You are an expert API architect and Node.js developer.

Design a RESTful API for:

User management system with authentication and profile management

Please provide:

1. **Endpoints**: RESTful routes with HTTP methods
   ```
   POST   /api/v1/auth/register     - User registration
   POST   /api/v1/auth/login        - User authentication
   POST   /api/v1/auth/logout       - User logout
   GET    /api/v1/users             - List users (admin)
   GET    /api/v1/users/:id         - Get user by ID
   PUT    /api/v1/users/:id         - Update user profile
   DELETE /api/v1/users/:id         - Delete user (admin)
   GET    /api/v1/users/me          - Get current user profile
   PUT    /api/v1/users/me/password - Change password
   ```

2. **Request/Response**: JSON schemas and examples
   - Request/response schemas for each endpoint
   - Example payloads with all required fields
   - Response format consistency
   - Pagination schemas for list endpoints

3. **Authentication**: Security considerations
   - JWT-based authentication strategy
   - Token refresh mechanism
   - Role-based access control (RBAC)
   - API key authentication for admin endpoints
   - Security headers and CORS configuration

4. **Validation**: Input validation rules
   - Email format validation
   - Password strength requirements
   - Required field validation
   - Data type and length constraints
   - Sanitization rules for user input

5. **Error Handling**: Error codes and messages
   ```json
   {
     "error": {
       "code": "VALIDATION_ERROR",
       "message": "Invalid input data",
       "details": [
         {
           "field": "email",
           "message": "Invalid email format"
         }
       ]
     }
   }
   ```

6. **Documentation**: OpenAPI/Swagger spec
   - Complete OpenAPI 3.0 specification
   - Interactive API documentation
   - Request/response examples
   - Authentication documentation
   - Error response documentation

7. **Implementation**: Node.js code examples
   - Express.js route handlers
   - Middleware implementation
   - Validation schemas (Joi/Yup)
   - Authentication middleware
   - Error handling middleware

**Additional Considerations:**
- Rate limiting implementation
- API versioning strategy
- Caching headers and strategies
- Monitoring and logging requirements
- Testing strategy for API endpoints

Follow REST principles including proper HTTP status codes, resource naming conventions, and stateless design patterns.
```

## When This Template Triggers

- Phrases like "API design", "REST API", "service design"
- Backend architecture requests
- API specification needs

## Benefits

- Ensures comprehensive API design
- Follows REST principles and conventions
- Includes security considerations
- Provides complete documentation approach
- Language-specific implementation guidance
- Covers error handling patterns
- Includes testing and monitoring aspects