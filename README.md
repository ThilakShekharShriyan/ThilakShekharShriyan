<div align="center">

# Thilak Shekhar Shriyan

*Systems. Memory, durability, and the tail of the latency distribution.*

[Systems](#systems) · [Run](#run) · [Elsewhere](#elsewhere)

</div>

Allocation, the log that has to survive a crash, and what to keep when the slow requests are the ones that matter.

## Systems

- **Memory.** A thread cache in front of one shared freelist, so the fast path does not take a lock. [memallocator](https://github.com/ThilakShekharShriyan/memallocator) is the Rust version: a slab, a lock-free queue, an epoch collector, and a Metal suballocator.
- **Durability.** Write the log before the page cache. Replicate it when it has to exist on more than one machine. Record a payment once. [BlitzLog](https://github.com/ThilakShekharShriyan/BlitzLog) is the compressed log with Raft. [PlayFlow](https://github.com/ThilakShekharShriyan/PlayFlow) is the Go ledger, double-entry, exactly-once.
- **The tail.** Evict for the p99, not the mean, and search with a vector score and a keyword score in the same store. [p99-edge-cache](https://github.com/ThilakShekharShriyan/p99-edge-cache) is the cache simulator. [EmbedBase](https://github.com/ThilakShekharShriyan/EmbedBase) is the Go index, HNSW plus BM25.

> [!TIP]
> [memallocator](https://github.com/ThilakShekharShriyan/memallocator) prints where the time went. Release is the number that matters.

## Run

```sh
git clone https://github.com/ThilakShekharShriyan/memallocator
cd memallocator
cargo test
cargo run --release
```

`cargo run --release -- gaps` prints the gaps between those choices. The longer cache sweep is [CCNFinalAssignment](https://github.com/ThilakShekharShriyan/CCNFinalAssignment).

## Elsewhere

<details>
<summary>Other work</summary>

Federated learning and agents: [FlowerHackathon](https://github.com/ThilakShekharShriyan/FlowerHackathon), [flower-grid-observability-demo](https://github.com/ThilakShekharShriyan/flower-grid-observability-demo), [akash-autopilot](https://github.com/ThilakShekharShriyan/akash-autopilot), [GeoScale](https://github.com/ThilakShekharShriyan/GeoScale).

Apps: [LecRef](https://github.com/ThilakShekharShriyan/LecRef), [link-road](https://github.com/ThilakShekharShriyan/link-road), [AlmaProject](https://github.com/ThilakShekharShriyan/AlmaProject), [GameScroll](https://github.com/ThilakShekharShriyan/GameScroll).

</details>

San Jose · [thilakshekharshriyan@gmail.com](mailto:thilakshekharshriyan@gmail.com) · [LinkedIn](https://www.linkedin.com/in/thilakshekharshriyan)
