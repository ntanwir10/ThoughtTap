# Database Design Template

**Category**: Architecture
**Tier**: Free
**Best For**: Designing database schemas and queries

## Description

Designs database solutions including schema design, relationships, indexing strategies, and query optimization. This template ensures your database design follows best practices for performance, scalability, and maintainability.

## Template

```
You are a database architect and {language} developer.

Design a database solution for:

{input}

Please provide:

1. **Schema Design**: Tables, relationships, and constraints
2. **Indexes**: Performance optimization strategies
3. **Queries**: Common SQL queries and optimizations
4. **Data Models**: {language} models/entities
5. **Migration Scripts**: Database setup and updates
6. **Best Practices**: Performance and security considerations

Consider scalability, normalization, and query performance.
```

## Variables

- `language` (string): Programming language for data models (automatically detected from context)

## Example Usage

### Input
```
design a database for an e-commerce system
```

### Optimized Output
```
You are a database architect and Node.js developer.

Design a database solution for:

E-commerce system with products, users, orders, and inventory management

Please provide:

1. **Schema Design**: Tables, relationships, and constraints
   ```sql
   -- Users table
   CREATE TABLE users (
     id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
     email VARCHAR(255) UNIQUE NOT NULL,
     password_hash VARCHAR(255) NOT NULL,
     first_name VARCHAR(100) NOT NULL,
     last_name VARCHAR(100) NOT NULL,
     created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
     updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );

   -- Products table
   CREATE TABLE products (
     id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
     name VARCHAR(255) NOT NULL,
     description TEXT,
     price DECIMAL(10,2) NOT NULL,
     category_id UUID REFERENCES categories(id),
     created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );

   -- Orders and relationships
   -- ... additional tables with proper constraints
   ```

2. **Indexes**: Performance optimization strategies
   - Primary key indexes (automatic)
   - Foreign key indexes for joins
   - Composite indexes for common query patterns
   - Partial indexes for filtered queries
   - Full-text search indexes for product searches

3. **Queries**: Common SQL queries and optimizations
   - Product search with filters and pagination
   - Order history with user details
   - Inventory management queries
   - Sales reporting and analytics
   - Performance-optimized joins

4. **Data Models**: Node.js models/entities
   ```javascript
   // Using Sequelize or Prisma
   const User = sequelize.define('User', {
     id: { type: DataTypes.UUID, primaryKey: true },
     email: { type: DataTypes.STRING, unique: true },
     // ... other fields
   });

   const Product = sequelize.define('Product', {
     // ... model definition
   });

   // Associations
   User.hasMany(Order);
   Order.belongsTo(User);
   ```

5. **Migration Scripts**: Database setup and updates
   - Initial schema creation
   - Version-controlled database changes
   - Data migration scripts
   - Rollback procedures
   - Environment-specific configurations

6. **Best Practices**: Performance and security considerations
   - Data normalization strategies
   - Query optimization techniques
   - Connection pooling configuration
   - Security measures (encryption, access control)
   - Backup and recovery procedures
   - Monitoring and alerting setup

**Additional Considerations:**
- Scalability patterns (read replicas, sharding)
- Caching strategies (Redis integration)
- Transaction management
- Data validation and constraints
- Audit logging and compliance
- Testing strategies for database operations

Consider ACID properties, proper normalization (3NF), and query performance optimization with appropriate indexing strategies.
```

## When This Template Triggers

- Phrases like "database", "schema", "data model", "SQL"
- Data architecture requests
- Database optimization needs

## Benefits

- Ensures proper database design principles
- Includes performance optimization strategies
- Provides migration and maintenance approaches
- Language-specific model implementations
- Covers security and scalability considerations
- Includes testing and monitoring aspects
- Follows normalization best practices