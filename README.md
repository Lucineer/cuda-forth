# cuda-forth

Minimal Forth-like agent language compiling to cuda-instruction-set bytecode. Stack-based, extensible, compact — the perfect agent language.

## Why Forth?

- **Stack-based** — matches the instruction set architecture directly
- **Extensible** — agents define their own words (become their own language)
- **Compact** — fits in memory-constrained edge environments
- **Self-hosting potential** — the language IS the agent

## Example

```forth
  : square DUP * ;
  : count-to-0 BEGIN DUP 0> WHILE 1- DUP . REPEAT DROP ;
  5 count-to-0    \ prints: 5 4 3 2 1

  \ Agent-specific words
  : sense-perceive CONF 0.95 SENSOR_ACQUIRE ;
  : deliberate CONF 0.5 DELIBERATE ;
  : tell-fleet CONF 0.8 BROADCAST "status update" ;
```

## Built-in Words

| Category | Words |
|----------|-------|
| Stack | DUP, DROP, SWAP, OVER, ROT |
| Arithmetic | ADD, SUB, MUL, DIV, MOD, NEG |
| Comparison | EQ, NEQ, LT, GT, LE, GE |
| Logic | AND, OR, XOR, NOT, SHL, SHR |
| Control | IF, THEN, ELSE, BEGIN, WHILE, REPEAT, UNTIL, DO, LOOP |
| A2A | TELL, ASK, BROADCAST |
| Biology | INSTINCT, GENE_EXPR, ENZYME_BIND, MEMBRANE_CHK |
| Energy | ATP_GEN, ATP_CONSUME, APOPTOSIS_CHK |
| Confidence | CONFIDENCE, TRUST, GATE, FUSE |
| I/O | EMIT, DOT, CR |

## Quick Start

```bash
git clone https://github.com/Lucineer/cuda-forth.git
cd cuda-forth
cargo test    # 13 tests
```

---

## Fleet Context

Part of the Lucineer/Cocapn fleet. See [fleet-onboarding](https://github.com/Lucineer/fleet-onboarding) for boarding protocol.

- **Vessel:** JetsonClaw1 (Jetson Orin Nano 8GB)
- **Domain:** Low-level systems, CUDA, edge computing
- **Comms:** Bottles via Forgemaster/Oracle1, Matrix #fleet-ops
