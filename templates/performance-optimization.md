# Performance Optimization Template

**Category**: Code Generation
**Tier**: Free
**Best For**: Optimizing code and system performance

## Description

Optimizes code and system performance by identifying bottlenecks, implementing improvements, and providing benchmarking strategies. This template focuses on language-specific optimizations and performance best practices.

## Template

```
You are a performance optimization expert in {language}.

Optimize the performance of:

{input}

Please analyze and provide:

1. **Performance Analysis**: Identify bottlenecks and issues
2. **Optimization Strategies**: Specific improvements
3. **Optimized Code**: Improved implementation
4. **Benchmarking**: How to measure improvements
5. **Trade-offs**: Performance vs other considerations
6. **Monitoring**: How to track performance in production

Focus on {language} specific optimizations and best practices.
```

## Variables

- `language` (string): Programming language for optimization (automatically detected from context)

## Example Usage

### Input

```
optimize this slow function
```

### Optimized Output

```
You are a performance optimization expert in JavaScript.

Optimize the performance of:

[Your slow function here]

Please analyze and provide:

1. **Performance Analysis**: Identify bottlenecks and issues
   - Algorithm complexity analysis (Big O notation)
   - Memory usage profiling
   - CPU-intensive operations identification
   - I/O bottlenecks and blocking operations
   - DOM manipulation inefficiencies (if applicable)
   - Network request optimization opportunities

2. **Optimization Strategies**: Specific improvements
   - Algorithm optimization (reduce time complexity)
   - Data structure improvements (use efficient collections)
   - Caching strategies (memoization, result caching)
   - Lazy loading and code splitting
   - Debouncing and throttling for user interactions
   - Web Workers for heavy computations
   - Database query optimization

3. **Optimized Code**: Improved implementation
   ```javascript
   // Before: O(n²) implementation
   function slowFunction(data) {
     // Inefficient nested loops
   }

   // After: O(n log n) optimized implementation
   function optimizedFunction(data) {
     // Efficient algorithm with better data structures
     // Includes memoization and early returns
   }
   ```

4. **Benchmarking**: How to measure improvements
   - Performance.now() for timing measurements
   - Chrome DevTools profiling
   - Memory usage monitoring
   - Lighthouse performance audits (for web apps)
   - Load testing with realistic data volumes
   - A/B testing for user-facing optimizations

5. **Trade-offs**: Performance vs other considerations
   - Code readability vs performance gains
   - Memory usage vs execution speed
   - Development complexity vs optimization benefits
   - Maintenance overhead of optimized code
   - Browser compatibility considerations

6. **Monitoring**: How to track performance in production
   - Performance metrics collection
   - Real User Monitoring (RUM) setup
   - Error rate and timeout tracking
   - Resource usage monitoring
   - Performance regression alerts
   - User experience metrics (Core Web Vitals)

**JavaScript-Specific Optimizations:**

- V8 engine optimization hints
- JIT compilation considerations
- Event loop and microtask optimization
- Bundle size reduction techniques
- Tree shaking and dead code elimination
- Service worker caching strategies

**Implementation Best Practices:**

- Avoid premature optimization
- Profile before optimizing
- Measure actual performance gains
- Consider user experience impact
- Document optimization decisions
- Plan for scalability requirements

Focus on measurable improvements and provide before/after performance comparisons with realistic test scenarios.

```

## When This Template Triggers

- Phrases like "performance", "optimize", "speed up", "slow", "bottleneck"
- Performance improvement requests
- Code efficiency needs

## Benefits

- Identifies specific performance bottlenecks
- Provides language-specific optimization strategies
- Includes benchmarking and measurement approaches
- Considers trade-offs and maintenance aspects
- Covers production monitoring requirements
- Focuses on measurable improvements
- Promotes evidence-based optimization
