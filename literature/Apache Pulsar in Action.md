---
type: book
subject: [[Pulsar]]
---

# Chapter 1 - Intro to Pulsar

## 1.3 Distributed message systems

p18 "Write-ahead log" is key architectural concept behind distributed message system

p20 Partition-based storage used in Kafka
- Partitions are a rigid concept - # parts determined on topic creation, limited by broker disk space, rebalance required on partition change

p22 (bottom) Segment-based storage in Pulsar
