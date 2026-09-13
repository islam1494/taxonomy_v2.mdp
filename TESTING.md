# Testing Guide

## Running Tests Locally

### All Tests
```bash
cargo test
```

### Specific Test Module
```bash
cargo test module_name
```

### With Output
```bash
cargo test -- --nocapture
```

### Single-threaded (for debugging)
```bash
cargo test -- --test-threads=1
```

## Code Coverage

Generate code coverage report:

```bash
cargo install cargo-tarpaulin
cargo tarpaulin --out Html
```

Then open `tarpaulin-report.html` in your browser.

## Performance Testing

Benchmark code performance:

```bash
cargo bench
```

## Security Testing

### Audit Dependencies
```bash
cargo audit
```

### Check Code Quality
```bash
cargo clippy
```

### Format Check
```bash
cargo fmt --check
```

## Before Submitting PR

1. ✅ Run all tests:
   ```bash
   cargo test --all-features
   ```

2. ✅ Format code:
   ```bash
   cargo fmt
   ```

3. ✅ Check with Clippy:
   ```bash
   cargo clippy --all-targets --all-features
   ```

4. ✅ Run security audit:
   ```bash
   cargo audit
   ```

5. ✅ Check coverage:
   ```bash
   cargo tarpaulin --out Stdout
   ```

## Test Structure

```
src/
├── lib.rs          # Library entry point
└── tests/          # Integration tests
    └── integration_test.rs
```

## Writing Tests

### Unit Tests
```rust
#[cfg(test)]
mod tests {
    use super::*;

    #[test]
    fn test_functionality() {
        let result = some_function();
        assert_eq!(result, expected_value);
    }
}
```

### Integration Tests
Create files in `tests/` directory:
```rust
// tests/integration_test.rs
#[test]
fn test_complete_workflow() {
    // Your integration test
}
```

## CI/CD Pipeline

Our GitHub Actions pipeline runs:
- ✅ Formatting checks (`cargo fmt`)
- ✅ Linting (`cargo clippy`)
- ✅ Tests on stable and beta
- ✅ Security audit
- ✅ Code coverage

All checks must pass before merging to main.

---

For more information, see [CONTRIBUTING.md](CONTRIBUTING.md)
