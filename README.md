# Krish Sarin

**Software engineer focused on backend systems and applied AI · Georgia Tech CS ’28**

My work focuses on building APIs, AI agents, data pipelines, and user-facing applications. I previously worked on Delta Air Lines’ Enterprise AI team and have also turned startup ideas and side projects into working software. I’m seeking 2027 software engineering internships in backend, AI, and full-stack development.

## Experience

- **Delta Air Lines** — Software Engineering Intern, Enterprise AI Team (2026)
- **Zayzen AI** — Software Engineering Intern (2025)
- **Emory University Biomedical Engineering** — Biomedical Engineering Researcher (2023–2024)
- **GreenEatsApp** — Co-Founder (2026–present) · [greeneatsapp.com](https://www.greeneatsapp.com)

## Projects

### [SentinelAI](https://github.com/ksarin10/sentinelAI)

Helps developers compare LLM response quality, latency, and cost through trace collection and prompt replay, with a Go ingestion gateway that preserves traces through outages.

`TypeScript` · `Go` · `Next.js` · `PostgreSQL` · `Redis`

[Reliability and benchmark report](https://github.com/ksarin10/sentinelAI/blob/main/docs/ingestion-reliability.md)

### [Relay](https://github.com/ksarin10/relay)

A C++20 TCP message broker with Go clients, durable at-least-once delivery, crash recovery, and backpressure, tested through reproducible failures and Linux benchmarks.

`C++20` · `Go` · `TCP` · `Linux` · `Concurrency`

[Benchmark report](https://github.com/ksarin10/relay/blob/main/BENCHMARK.md) · [Failure contract](https://github.com/ksarin10/relay/blob/main/docs/failure-semantics.md)

### [Sensor Recovery](https://github.com/ksarin10/sensor-recovery)

A PyTorch study of recovering missing motion-sensor data, comparing an autoencoder and conditional diffusion with simple baselines while measuring reconstruction error, activity recognition, and latency.

`Python` · `PyTorch` · `Time-series ML` · `Experimental design`

[Experiment report](https://github.com/ksarin10/sensor-recovery/blob/main/results/REPORT.md)

### [Prostate Cancer Detection](https://github.com/ksarin10/Prostate-Cancer-Detection-Model)

Computer-vision research at Emory combining whole-slide image preprocessing, stain normalization, U-Net cancer segmentation, and reconstruction of patch predictions into whole-slide masks.

`Python` · `TensorFlow` · `OpenCV` · `OpenSlide`

## Earlier research

**[Financial Fraud Detection](https://github.com/ksarin10/Finance-Fraud)** — Compared five anomaly-detection methods, including a TensorFlow autoencoder, on synthetic credit-card transactions using shared preprocessing and precision, recall, and F1 evaluation.

## What I work with

- **Systems and backend:** C++20, Go, TypeScript, Python, TCP, REST APIs, concurrency
- **Data and infrastructure:** PostgreSQL, Prisma, Redis, BullMQ, Linux, Docker, GitHub Actions
- **Applied ML:** PyTorch, LLM evaluation, time-series reconstruction, computer vision, experiment design

## Engineering approach

I define failure behavior before adding features, test the paths that can lose data, measure before optimizing, and report limitations alongside results.
