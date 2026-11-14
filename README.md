# Krish Sarin

**Software engineer focused on backend systems and applied AI · Georgia Tech CS ’28**

My work focuses on building APIs, AI agents, data pipelines, and user-facing applications. I previously worked on Delta Air Lines’ Enterprise AI team and have also turned startup ideas and side projects into working software. I’m seeking 2027 software engineering internships in backend, AI, and full-stack development.

## Experience

- **Delta Air Lines** — Software Engineering Intern, Enterprise AI Team (2026)
- **Zayzen AI** — Software Engineering Intern (2025)
- **Emory University Biomedical Engineering** — Research Assistant (2023–2024)
- **GreenEatsApp** — Co-Founder (2026–present) · [greeneatsapp.com](https://www.greeneatsapp.com)

## Selected projects

### [SentinelAI](https://github.com/ksarin10/sentinelAI)

Verified model switching for LLM applications. SentinelAI ingests production traces, identifies lower-cost model candidates, runs shadow replays, and returns recommendations backed by replay-level quality and failure evidence.

- Built a Go ingestion gateway with AES-GCM encryption, an fsync-backed spool, bounded per-key capacity, retries, and durable dead letters.
- A process-kill recovery experiment durably accepted 500 traces during an outage and recovered 500 unique downstream effects with zero loss.
- CPU profiling found disk lookups dominating duplicate detection; an in-memory key index made the path 30.9× faster while preserving the durability boundary.

`TypeScript` · `Go` · `NestJS` · `Next.js` · `PostgreSQL` · `Redis` · `BullMQ` · `Docker`

[Reliability and benchmark report](https://github.com/ksarin10/sentinelAI/blob/main/docs/ingestion-reliability.md)

### [Relay](https://github.com/ksarin10/relay)

A fault-tolerant TCP message broker with a C++20 server and Go clients. Relay uses an append-only log, acknowledgements, bounded backpressure, message IDs, and at-least-once redelivery across disconnects and broker restarts.

- Handles partial TCP reads and writes, concurrent producers, slow consumers, torn log records, overload, and persistence failures.
- Fault tests use real sockets, `SIGKILL`, forced partial disk writes, reconnects, and replay; the project also passes address, undefined-behavior, thread, and Go race sanitizers.
- Linux measurements reached a median 2,056 durable messages/second with 6.5 ms p99 latency and 56 ms recovery from a 10,000-message log.

`C++20` · `Go` · `TCP` · `Linux` · `Concurrency` · `Docker` · `GitHub Actions`

[Benchmark report](https://github.com/ksarin10/relay/blob/main/BENCHMARK.md) · [Failure contract](https://github.com/ksarin10/relay/blob/main/docs/failure-semantics.md)

### [Sensor Recovery](https://github.com/ksarin10/sensor-recovery)

A PyTorch study of methods for reconstructing missing wearable accelerometer and gyroscope data while preserving downstream activity recognition. It compares zero filling, interpolation, a denoising autoencoder, and conditional diffusion on participant-separated UCI HAPT data.

- Split participants before creating overlapping windows and computed normalization from training participants only.
- The autoencoder retained 0.997 macro F1 on 32-sample gaps and 0.932 on unseen 64-sample gaps; interpolation remained best for isolated random loss.
- Stopped the diffusion sweep after it was roughly 149× slower than the autoencoder with worse reconstruction error, documenting the negative result instead of presenting it as an improvement.

`Python` · `PyTorch` · `Time-series ML` · `Experimental design` · `pytest`

[Experiment report](https://github.com/ksarin10/sensor-recovery/blob/main/results/REPORT.md)

## What I work with

- **Systems and backend:** C++20, Go, TypeScript, Python, TCP, REST APIs, concurrency
- **Data and infrastructure:** PostgreSQL, Prisma, Redis, BullMQ, Linux, Docker, GitHub Actions
- **Applied ML:** PyTorch, LLM evaluation, time-series reconstruction, computer vision, experiment design

## Engineering approach

I define failure behavior before adding features, test the paths that can lose data, measure before optimizing, and report limitations alongside results.
