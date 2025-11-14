# Security Review Template

**Category:** Code Review
**Tier:** Free
**Best For:** Identifying security vulnerabilities and implementing best practices

## Template Description

Reviews code for security vulnerabilities, authentication/authorization issues, data protection concerns, and provides actionable remediation steps with secure code examples.

## How It Works

This template transforms simple security review requests into comprehensive security audits by analyzing:

1. **Vulnerability Assessment** - Common security flaws and attack vectors
2. **Input Validation** - Data sanitization and validation techniques
3. **Authentication/Authorization** - Access control and permission issues
4. **Data Protection** - Encryption, sensitive data handling, and storage
5. **Security Best Practices** - Language-specific security recommendations
6. **Remediation** - Step-by-step fixes with secure code examples

## When To Use

- 🔒 Reviewing code for security vulnerabilities before deployment
- 🛡️ Implementing authentication or authorization systems
- 🔐 Handling sensitive data (passwords, API keys, PII)
- 🚨 Responding to security audit findings
- ✅ Following security best practices for your tech stack
- 📋 Preparing for security compliance (SOC2, HIPAA, etc.)

## Example Input

```
Review this login function for security issues:

function login(username, password) {
  const query = `SELECT * FROM users WHERE username = '${username}' AND password = '${password}'`;
  const user = db.query(query);
  if (user) {
    return { success: true, token: username };
  }
  return { success: false };
}
```

## Example Output

```
You are a cybersecurity expert specializing in JavaScript applications.

Perform a security review of:

function login(username, password) {
  const query = `SELECT * FROM users WHERE username = '${username}' AND password = '${password}'`;
  const user = db.query(query);
  if (user) {
    return { success: true, token: username };
  }
  return { success: false };
}

Please analyze:

1. **Vulnerability Assessment**: Common security flaws
   - SQL Injection vulnerability (CRITICAL)
   - Plaintext password comparison (HIGH)
   - Weak authentication token (HIGH)
   - No rate limiting or brute force protection (MEDIUM)

2. **Input Validation**: Data sanitization and validation
   - Missing input validation for username and password
   - No length limits or character restrictions
   - Vulnerable to SQL injection attacks

3. **Authentication/Authorization**: Access control issues
   - No password hashing (bcrypt, argon2, etc.)
   - Token uses predictable username instead of secure JWT
   - No session management or expiration
   - Missing multi-factor authentication support

4. **Data Protection**: Encryption and sensitive data handling
   - Passwords stored/compared in plaintext
   - No encryption for authentication tokens
   - Missing HTTPS enforcement
   - No protection against timing attacks

5. **Security Best Practices**: JavaScript specific recommendations
   - Use parameterized queries or ORM to prevent SQL injection
   - Implement password hashing with bcrypt (12+ rounds)
   - Generate secure JWTs with proper expiration
   - Add rate limiting middleware (express-rate-limit)
   - Implement account lockout after failed attempts
   - Use helmet.js for security headers
   - Enable CORS properly
   - Implement CSRF protection

6. **Remediation**: Step-by-step fixes with secure code examples

**Step 1: Fix SQL Injection (CRITICAL)**
```javascript
// SECURE: Use parameterized queries
async function login(username, password) {
  const query = 'SELECT * FROM users WHERE username = ?';
  const [users] = await db.execute(query, [username]);
  // ...
}
```

**Step 2: Implement Password Hashing (HIGH)**
```javascript
const bcrypt = require('bcrypt');

// When creating user
const hashedPassword = await bcrypt.hash(password, 12);

// When verifying
const isValid = await bcrypt.compare(password, user.password_hash);
```

**Step 3: Generate Secure Tokens (HIGH)**
```javascript
const jwt = require('jsonwebtoken');

if (isValid) {
  const token = jwt.sign(
    { userId: user.id, username: user.username },
    process.env.JWT_SECRET,
    { expiresIn: '1h', algorithm: 'HS256' }
  );
  return { success: true, token };
}
```

**Step 4: Add Rate Limiting (MEDIUM)**
```javascript
const rateLimit = require('express-rate-limit');

const loginLimiter = rateLimit({
  windowMs: 15 * 60 * 1000, // 15 minutes
  max: 5, // 5 attempts
  message: 'Too many login attempts, please try again later'
});

app.post('/login', loginLimiter, loginHandler);
```

**Complete Secure Implementation:**
```javascript
const bcrypt = require('bcrypt');
const jwt = require('jsonwebtoken');
const rateLimit = require('express-rate-limit');

const loginLimiter = rateLimit({
  windowMs: 15 * 60 * 1000,
  max: 5
});

async function login(username, password) {
  // Input validation
  if (!username || !password) {
    throw new Error('Username and password required');
  }

  if (username.length > 100 || password.length > 100) {
    throw new Error('Invalid input length');
  }

  // Parameterized query
  const query = 'SELECT id, username, password_hash FROM users WHERE username = ?';
  const [users] = await db.execute(query, [username]);

  if (users.length === 0) {
    // Use constant-time comparison to prevent timing attacks
    await bcrypt.compare(password, '$2b$12$dummyhashtopreventtimingattack');
    return { success: false, message: 'Invalid credentials' };
  }

  const user = users[0];

  // Verify password with bcrypt
  const isValid = await bcrypt.compare(password, user.password_hash);

  if (!isValid) {
    return { success: false, message: 'Invalid credentials' };
  }

  // Generate secure JWT
  const token = jwt.sign(
    { userId: user.id, username: user.username },
    process.env.JWT_SECRET,
    { expiresIn: '1h', algorithm: 'HS256' }
  );

  return {
    success: true,
    token,
    expiresIn: 3600
  };
}

module.exports = { login, loginLimiter };
```

Prioritize findings by severity and provide actionable solutions.
```

## Variables

- `{language}` - Programming language (auto-detected from project context)
- `{input}` - Your code or security question

## Related Templates

- **Code Review** - General code quality and best practices review
- **Testing** - Create comprehensive tests including security test cases
- **Refactoring** - Refactor code to address security concerns

## Tips

- Be specific about the type of security concern (auth, data protection, etc.)
- Provide surrounding context (database type, framework, dependencies)
- Mention compliance requirements if applicable (HIPAA, GDPR, etc.)
- Include any existing security measures already in place
