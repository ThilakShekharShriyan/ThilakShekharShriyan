<div align="center">

# Thilak Shekhar Shriyan

*Rust for the path that has to stay correct while it is fast.*

[![Rust](https://img.shields.io/badge/Rust-allocators%20%C2%B7%20logs%20%C2%B7%20tail%20latency-111111?style=flat-square&logo=rust&logoColor=white)](https://github.com/ThilakShekharShriyan/memallocator)

[Crates](#crates) · [Run](#run) · [Elsewhere](#elsewhere)

</div>

Allocators, logs, lock-free structures, and the tail of a latency distribution. Safe Rust owns the algorithm. `unsafe` stays on the slab backing store, the queue slot, the retired map node, and a Metal timestamp. Each of those sites says which invariant makes it sound.

> [!TIP]
> Release is the number that matters. Debug builds keep double-free checks and do not inline the same way.

## Features

- **Thread-cached allocation.** A hit stays on a thread-local stack. A miss refills 32 blocks from one shared freelist. The slab covers 16 to 2048 bytes.
- **Durable logs.** Delta and varint encoding, SIMD scans, a write-ahead log, and Raft when the log has to live on more than one machine.
- **Tail latency.** Evict for the p99, not the mean.

## Crates

### [memallocator](https://github.com/ThilakShekharShriyan/memallocator)

A slab allocator with a thread-local magazine, a lock-free queue, two maps, an epoch collector, a page cache with a write-ahead log, and a Metal suballocator. Eight threads allocate and free 64-byte blocks, then the program prints where the time went.

### [BlitzLog](https://github.com/ThilakShekharShriyan/BlitzLog)

A compressed log engine. Delta and varint encoding, SIMD scans, a write-ahead log, and Raft.

### [p99-edge-cache](https://github.com/ThilakShekharShriyan/p99-edge-cache)

A chunk-cache simulator. LRU and LFU against a policy that evicts from the tail. The longer sweep is [CCNFinalAssignment](https://github.com/ThilakShekharShriyan/CCNFinalAssignment).

## Run

```sh
git clone https://github.com/ThilakShekharShriyan/memallocator
cd memallocator
cargo test
cargo run --release
```

`cargo run --release -- gaps` prints the gaps between those choices.

## Elsewhere

Same questions in Go: [PlayFlow](https://github.com/ThilakShekharShriyan/PlayFlow) is a double-entry payment ledger with exactly-once handling, and [EmbedBase](https://github.com/ThilakShekharShriyan/EmbedBase) is an embeddable vector index with HNSW, BM25, and a write-ahead log.

<details>
<summary>Other work</summary>

Federated learning and agents: [FlowerHackathon](https://github.com/ThilakShekharShriyan/FlowerHackathon), [flower-grid-observability-demo](https://github.com/ThilakShekharShriyan/flower-grid-observability-demo), [akash-autopilot](https://github.com/ThilakShekharShriyan/akash-autopilot), [GeoScale](https://github.com/ThilakShekharShriyan/GeoScale).

Apps: [LecRef](https://github.com/ThilakShekharShriyan/LecRef), [link-road](https://github.com/ThilakShekharShriyan/link-road), [AlmaProject](https://github.com/ThilakShekharShriyan/AlmaProject), [GameScroll](https://github.com/ThilakShekharShriyan/GameScroll).

</details>

San Jose · [thilakshekharshriyan@gmail.com](mailto:thilakshekharshriyan@gmail.com) · [LinkedIn](https://www.linkedin.com/in/thilakshekharshriyan)
