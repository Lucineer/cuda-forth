# cuda-forth

Minimal Forth-like agent language — stack-based, extensible, compiles to instruction-set bytecode (Rust)

Part of the Cocapn build layer — compilers, assemblers, and code transformation.

## What It Does

### Key Types

- `Word` — core data structure
- `Forth` — core data structure

## Quick Start

```bash
# Clone
git clone https://github.com/Lucineer/cuda-forth.git
cd cuda-forth

# Build
cargo build

# Run tests
cargo test
```

## Usage

```rust
use cuda_forth::*;

// See src/lib.rs for full API
// 18 unit tests included
```

### Available Implementations

- `Builtin` — see source for methods
- `Forth` — see source for methods

## Testing

```bash
cargo test
```

18 unit tests covering core functionality.

## Architecture

This crate is part of the **Cocapn Fleet** — a git-native multi-agent ecosystem.

- **Category**: build
- **Language**: Rust
- **Dependencies**: See `Cargo.toml`
- **Status**: Active development

## Related Crates

- [cuda-bytecode-optimizer](https://github.com/Lucineer/cuda-bytecode-optimizer)
- [cuda-asm](https://github.com/Lucineer/cuda-asm)
- [cuda-equipment](https://github.com/Lucineer/cuda-equipment)

## Fleet Position

```
Casey (Captain)
├── JetsonClaw1 (Lucineer realm — hardware, low-level systems, fleet infrastructure)
├── Oracle1 (SuperInstance — lighthouse, architecture, consensus)
└── Babel (SuperInstance — multilingual scout)
```

## Contributing

This is a fleet vessel component. Fork it, improve it, push a bottle to `message-in-a-bottle/for-jetsonclaw1/`.

## License

MIT

---

*Built by JetsonClaw1 — part of the Cocapn fleet*
*See [cocapn-fleet-readme](https://github.com/Lucineer/cocapn-fleet-readme) for the full fleet roadmap*
