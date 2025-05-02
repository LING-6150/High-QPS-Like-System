
# High-QPS Like System

A high-performance backend service for processing user "like" interactions at scale, designed to handle **5,000+ QPS per node** with robust caching, messaging, and observability infrastructure.

## 🚀 Features

- ⚡ **High Concurrency Support**: Designed for 5K+ QPS with Redis+Caffeine multi-level caching
- 💾 **Cache Consistency**: Lua-based atomic Redis ops + HeavyKeeper hot key detection
- 📨 **Asynchronous Processing**: Integrated Apache Pulsar for decoupled like event handling
- 🧠 **Duplicate Protection**: Fingerprint deduplication to ensure idempotent operations
- 📊 **Monitoring & Resilience**: Built-in Prometheus/Grafana metrics, chaos engineering, and failover strategies
- ☁️ **Cloud Ready**: Dockerized deployment with Nginx load balancing

## 🛠️ Tech Stack

- **Backend**: Java, Spring Boot
- **Caching**: Redis, Caffeine
- **Messaging**: Apache Pulsar
- **Storage**: TiDB / MySQL
- **Observability**: Prometheus, Grafana
- **Deployment**: Docker, Nginx

## 📂 Project Structure

```
high-qps-like-system/
├── src/
│   ├── main/
│   │   ├── java/
│   │   └── resources/
├── docker/
├── scripts/
└── README.md
```

## 📈 Metrics Tracked

| Metric                    | Value        |
|---------------------------|--------------|
| Max QPS (single node)     | 5,200+       |
| Avg latency (p99)         | 32ms         |
| DB Load Reduction         | -80%         |
| Cache Penetration         | ~0% (HeavyKeeper) |
| MTTR                      | ↓ 85%        |

## 📦 Deployment

```bash
docker-compose up -d
```

## 👤 Author

- Ling Duan | [GitHub](https://github.com/LING-6150) | [LinkedIn](https://www.linkedin.com/in/lingduan/)

---
