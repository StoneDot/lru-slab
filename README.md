# Lru slab

Pre-allocated storage for a uniform data type.

[![Crates.io](https://img.shields.io/crates/v/slab.svg?maxAge=2592000)](https://crates.io/crates/slab)
[![Build Status](https://travis-ci.org/StoneDot/lru-slab.svg?branch=master)](https://travis-ci.org/StoneDot/lru-slab)

[Documentation](https://docs.rs/lru-slab/0.1.0/lru-slab/)

## Usage

To use `lru-slab`, first add this to your `Cargo.toml`:

```toml
[dependencies]
lru-slab = "0.0.1"
```

Next, add this to your crate:

```rust
extern crate lru_slab;

use lru_slab::LruSlab;

let mut slab = LruSlab::new();

let hello = slab.insert("hello");
let world = slab.insert("world");

assert_eq!(slab[hello], "hello");
assert_eq!(slab[world], "world");

slab[world] = "earth";
assert_eq!(slab[world], "earth");
```

See [documentation](https://docs.rs/lru-slab) for more details.

## License

This project is licensed under the [MIT license](LICENSE).

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in `lru-slab` by you, shall be licensed as MIT, without any additional
terms or conditions.
