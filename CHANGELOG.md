# Changelog

Notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Added
- Architecture-specific detail API
- Detail API unit tests

## [0.2.0] - 2017-11-01
### Added
- `Capstone::new_raw()` has the same interface as the old `Capstone::new_raw()`
- Add setters to modify mode, syntax, etc.

### Changed
- `Capstone::new()` uses the builder pattern
- Partition `Mode` enum into: `Mode`, `ExtraMode`, and `Endian`
- Rename `Capstone` methods that return IDs to include `_ids` in name
    - Example: `read_registers()` renamed to `read_register_ids()`

## [0.1.0] - 2017-09-29
### Added
- `Capstone` methods to set syntax and mode
- Travis continuous integration

### Changed
- Use [`capstone-sys`](https://github.com/capstone-rust/capstone-sys) crate for low-level Capstone bindings
- `Capstone::new()` takes a `arch` and `mode` arguments
- `Capstone::disasm()` replaced with `Capstone::disasm_all()`/`Capstone::disasm_count()`

### Removed
- Dependency

[Unreleased]: https://github.com/capstone-rust/capstone-rs/compare/v0.2.0...HEAD
[0.2.0]: https://github.com/capstone-rust/capstone-rs/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/capstone-rust/capstone-rs/releases/tag/v0.1.0
