# High-Throughput Real-Time Anomaly Detector

**Built a fault-tolerant distributed system processing 100,000+ msg/s with Apache Kafka + Python Asyncio**

## Architecture
## Tech Stack
- **Kafka 7.5** with `aiokafka` for async, non-blocking I/O
- **Python 3.11 + Asyncio**: Handles 100k+ msg/s per consumer
- **Welford's Algorithm**: O(1) anomaly detection without sliding windows
- **PostgreSQL 15**: Idempotent inserts via `ON CONFLICT DO NOTHING`
- **Docker Compose**: One-command deployment of full stack
- **Fault Tolerance**: Dead Letter Queue + exponential backoff + graceful shutdown

## Run Locally
```bash
git clone https://github.com/mostafasinaiepur-lang/kafka-zscore-anomaly-detector.git
cd kafka-zscore-anomaly-detector
docker-compose up --build