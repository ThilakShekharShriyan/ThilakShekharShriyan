# Thilak Shekhar Shriyan

I build systems software: memory allocators, log engines, vector search, and the control paths around training and inference.

I am in the MS Computer Science program at San Jose State University (2025–2027). I studied computer science at PES University (2019–2023), worked as a software engineer at Couchbase, and in summer 2026 worked at AWS on session placement for a distributed compute fleet.

San Jose, CA · [LinkedIn](https://www.linkedin.com/in/thilakshekharshriyan) · [thilakshekharshriyan@gmail.com](mailto:thilakshekharshriyan@gmail.com) · [Portfolio](https://portfolio-website-thilakshekharshriyan.vercel.app/)

## Interests

Memory and concurrency, databases, distributed systems, and machine-learning infrastructure. Recent projects are mostly Rust and Go. Python is what I use for training, federated learning, and agents.

## Experience

**Software Development Engineer, Amazon Web Services** · May 2026 – Aug 2026

Designed a Rust session-placement engine for a distributed compute fleet: bin-packing, spread, and affinity-aware scheduling. The concurrent path uses Tokio and Crossbeam. Telemetry ingestion is zero-copy, and placement state is stored in Aurora DSQL.

**Software Engineer, Couchbase** · Jan 2023 – Aug 2025

Ran customer-facing services on Linux, AWS, Docker, and EKS. Built log-ingestion pipelines, wired Prometheus, Grafana, and Datadog, and raised Go backend throughput with tighter concurrency and buffer use. Worked on distributed vector retrieval with FAISS, Elasticsearch, and SQL.

**Earlier**

Summer internship at Accenture on collecting and delivering data from more than one source. At PESU Venture Labs I built Flutter pages for Teaminup on MongoDB and GraphQL, and wrote Python scrapers whose output fed startup models.

## Projects

### Systems

| Project | What it is |
| --- | --- |
| [memallocator](https://github.com/ThilakShekharShriyan/memallocator) | Rust slab allocator with a thread cache, lock-free queue, epoch collector, write-ahead log, and a Metal GPU suballocator. |
| [BlitzLog](https://github.com/ThilakShekharShriyan/BlitzLog) | Compressed log store in Rust: delta and varint encoding, SIMD queries, a write-ahead log, and Raft replication. |
| [PlayFlow](https://github.com/ThilakShekharShriyan/PlayFlow) | Payment orchestration in Go with a double-entry ledger and exactly-once handling from authorization through refund. |
| [EmbedBase](https://github.com/ThilakShekharShriyan/EmbedBase) | Embeddable hybrid vector store in Go: HNSW and IVF indexes, BM25, and a write-ahead log. |
| [p99-edge-cache](https://github.com/ThilakShekharShriyan/p99-edge-cache) | Edge cache simulator comparing LRU, LFU, and a p99-aware eviction policy. Coursework for CS 258 at SJSU. The fuller sweep is in [CCNFinalAssignment](https://github.com/ThilakShekharShriyan/CCNFinalAssignment). |
| [TILUDistributedSystems](https://github.com/ThilakShekharShriyan/TILUDistributedSystems) | Reading notes on how companies split their distributed systems, taken from public write-ups. |
| [MiniMicroServices](https://github.com/ThilakShekharShriyan/MiniMicroServices) | Small Go implementations of distributed-systems pieces, starting with consistent hashing. |

### Machine learning and agents

| Project | What it is |
| --- | --- |
| [GeoScale](https://github.com/ThilakShekharShriyan/GeoScale) | Training pipeline for geospatial vision models: Ray ingestion, geohash shards, ViT training, and FAISS retrieval. |
| [FlowerHackathon](https://github.com/ThilakShekharShriyan/FlowerHackathon) | Terminal agent that runs Flower federated-learning experiments, logs them to MongoDB, and proposes the next config. |
| [flower-grid-observability-demo](https://github.com/ThilakShekharShriyan/flower-grid-observability-demo) | Operator desk and runbooks for a Flower agent grid. |
| [akash-autopilot](https://github.com/ThilakShekharShriyan/akash-autopilot) | Agent that watches Akash deployments and scales or redeploys them inside policy limits. |
| [LecRef](https://github.com/ThilakShekharShriyan/LecRef) | Lecture companion that transcribes speech, defines terms as they come up, and writes cited research notes. [Live demo](https://v0-lec-ref.vercel.app). |
| [link-road](https://github.com/ThilakShekharShriyan/link-road) | Road-scene demo: in-browser YOLO, a simulated multi-lane road, and a voice and video agent for hazards such as potholes and debris. |
| [GoLLMServe](https://github.com/ThilakShekharShriyan/GoLLMServe) | Notes toward an LLM serving engine in Go with a distributed KV cache. |
| [Cataract-Detection---Capstone](https://github.com/ThilakShekharShriyan/Cataract-Detection---Capstone) | Flask app for cataract detection. |
| [ImageCaptionGenerator](https://github.com/ThilakShekharShriyan/ImageCaptionGenerator) | Image captions with a VGG19 CNN: images are vectorized and matched to caption text. |
| [ImageClassificationWebsite](https://github.com/ThilakShekharShriyan/ImageClassificationWebsite) | Website for image classification. |
| [Fedrated-Learning-Client-Server-Architecture-](https://github.com/ThilakShekharShriyan/Fedrated-Learning-Client-Server-Architecture-) | Early client-server federated learning setup. |
| [Leads-Scoring-Data-Analytics](https://github.com/ThilakShekharShriyan/Leads-Scoring-Data-Analytics) | Lead-scoring analysis in notebooks. |

### Applications

| Project | What it is |
| --- | --- |
| [AlmaProject](https://github.com/ThilakShekharShriyan/AlmaProject) | Lead intake for an attorney: public application, resume upload, email, and a signed-in review queue. [Live site](https://leads.thilakshekharshriyan.com). |
| [GameScroll](https://github.com/ThilakShekharShriyan/GameScroll) | Feed for scrolling through and creating small JavaScript games with Gemini. |
| [portfolioWebsite](https://github.com/ThilakShekharShriyan/portfolioWebsite) | Next.js portfolio backed by GraphCMS. [Site](https://portfolio-website-thilakshekharshriyan.vercel.app/). |
| [Bloggin-App](https://github.com/ThilakShekharShriyan/Bloggin-App) | Blogging app in Next.js. |
| [cf_ai_BlogMaker](https://github.com/ThilakShekharShriyan/cf_ai_BlogMaker) | Helper for updating blog posts. |
| [MERNstackmoviesearch](https://github.com/ThilakShekharShriyan/MERNstackmoviesearch) | Movie search with the MERN stack. |
| [Sorting_visualiser](https://github.com/ThilakShekharShriyan/Sorting_visualiser) | React sorting visualizer. |
| [AWS-CICD-pipeline](https://github.com/ThilakShekharShriyan/AWS-CICD-pipeline) | CI/CD pipeline on AWS. |

### Practice

- [Neetcode](https://github.com/ThilakShekharShriyan/Neetcode) — NeetCode problems in Python.
- [Go-Projects](https://github.com/ThilakShekharShriyan/Go-Projects) — Go exercises.
- [Blockchain](https://github.com/ThilakShekharShriyan/Blockchain) and [Solidity](https://github.com/ThilakShekharShriyan/Solidity) — blockchain and Solidity notes.
- [TextEncryption](https://github.com/ThilakShekharShriyan/TextEncryption) and [ImageEncryptionDecryption](https://github.com/ThilakShekharShriyan/ImageEncryptionDecryption) — encryption exercises.
- [swarm-learning](https://github.com/ThilakShekharShriyan/swarm-learning) — fork of a decentralized, privacy-preserving machine-learning library, from when I was learning that setup.

## Stack

**Languages.** Rust, C/C++, Go, Python, JavaScript/TypeScript, SQL, Shell.

**Data and search.** PostgreSQL, MySQL, MongoDB, Couchbase, Redis, Elasticsearch, FAISS.

**ML.** PyTorch, TensorFlow, scikit-learn, federated learning, RAG, LangChain, LlamaIndex.

**Infrastructure.** AWS, Docker, Kubernetes, Linux, Prometheus, Grafana, Datadog.

**Apps.** React, Next.js, REST.
