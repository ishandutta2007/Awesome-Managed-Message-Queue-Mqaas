# Awesome-Managed-Message-Queue-Mqaas

## Top Managed Message Queue (MQaaS) Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Message Queuing as a Service, Cloud Brokers & Self-Hosted Alternatives*  

**Last updated: October 2026**



This repository tracks notable **commercial Message Queuing as a Service (MQaaS) platforms** and **open-source projects** that provide managed message brokers, queues, and pub/sub messaging — enabling asynchronous communication, workload decoupling, and event-driven architectures without operating broker infrastructure.



**Examples** include Amazon SQS, RabbitMQ Cloud (CloudAMQP), Apache Kafka Cloud (Confluent), Google Cloud Pub/Sub, Azure Service Bus, Upstash QStash, IronMQ, ActiveMQ Cloud, Redpanda Cloud, and Amazon MQ (the category leaders).



**Open-source emphasis**: MQaaS is anchored by **RabbitMQ** as the most widely deployed open-source broker, **Apache Kafka** and **Apache Pulsar** for high-throughput streaming, **NATS** for cloud-native messaging, and **Apache ActiveMQ**/**Artemis** for JMS compliance. **Redis** powers lightweight task queues via BullMQ and Celery. **NSQ**, **Beanstalkd**, and **ZeroMQ** offer specialized alternatives. **KubeMQ** brings Kubernetes-native queuing. This section is heavily expanded.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Amazon SQS](https://aws.amazon.com/sqs/)**  

  **AWS's fully managed message queuing service** — standard and FIFO queues with at-least-once and exactly-once processing . **Dead letter queues, visibility timeouts, and long polling** . **Scales to virtually unlimited throughput** . **The reference for managed queuing** . **Best for AWS-native applications** .



- **[RabbitMQ Cloud (CloudAMQP)](https://www.cloudamqp.com/)**  

  **Managed RabbitMQ** — AMQP, MQTT, STOMP, and WebSocket support . **Reliable queuing with flexible routing** . **Best for traditional message queuing** .



- **[Apache Kafka Cloud (Confluent Cloud)](https://www.confluent.io/confluent-cloud/)**  

  **The leading managed Kafka platform** — fully managed Kafka, ksqlDB, Flink, connectors, and schema registry . **Created by Kafka's original developers** . **Best for enterprise event streaming** .



- **[Google Cloud Pub/Sub](https://cloud.google.com/pubsub)**  

  **Google's asynchronous messaging service** — global scale with at-least-once delivery . **Dead letter topics and retry policies** . **Best for GCP-native messaging** .



- **[Azure Service Bus](https://azure.microsoft.com/en-us/products/service-bus/)**  

  **Microsoft's message broker with DLQ** — automatic dead-lettering for expired, max-delivery, and filtering failures . **Queues and topics with sessions** . **Best for Azure-native messaging** .



- **[Upstash QStash](https://upstash.com/qstash)**  

  **Serverless message queue and scheduler** — HTTP-based with retries and delays . **Best for serverless event-driven workflows** .



- **[IronMQ](https://www.iron.io/)**  

  **Cloud-native message queue** — reliable message delivery with long polling and push queues . **Best for cloud-native applications** .



- **[ActiveMQ Cloud](https://activemq.apache.org/)**  

  **Managed ActiveMQ** — JMS, AMQP, MQTT, and STOMP support . **Best for JMS-based messaging** .



- **[Redpanda Cloud](https://redpanda.com/)**  

  **Kafka-compatible streaming platform in C++** — no Zookeeper, no JVM . **Best for high-performance streaming** .



- **[Amazon MQ](https://aws.amazon.com/amazon-mq/)**  

  **Managed ActiveMQ and RabbitMQ** — includes broker-level DLQ and retry configuration . **Best for managed message brokers** .



## Open-Source GitHub Projects



### Message Brokers



- **[RabbitMQ](https://github.com/rabbitmq/rabbitmq-server)**  

  **The most widely deployed open-source message broker**, MPL-2.0 licensed with **12,000+ GitHub stars** . **AMQP, MQTT, STOMP, and WebSocket support** . **Dead letter exchanges (DLX)** — messages that are rejected, expire, or exceed queue length can be routed to a DLX . **TTL (Time-To-Live) per message and per queue** . **Flexible routing with exchanges** . **Best for reliable message queuing with DLQ** .



- **[Apache Kafka](https://github.com/apache/kafka)**  

  **The de facto standard for event streaming**, Apache-2.0 licensed with **28,000+ GitHub stars** . **Distributed, fault-tolerant, high-throughput pub/sub messaging** . **Kafka Connect for source/sink connectors** . **DLQ patterns via Kafka Connect** . **Best for high-throughput event streaming** .



- **[Apache Pulsar](https://github.com/apache/pulsar)**  

  **Distributed messaging and streaming platform**, Apache-2.0 licensed with **14,000+ GitHub stars** . **Multi-tenancy, geo-replication, and tiered storage** . **Negative acknowledgment (nack)** and **Dead letter topic (DLT)** . **Best for multi-tenant messaging with built-in DLQ** .



- **[NATS](https://github.com/nats-io/nats-server)**  

  **Cloud-native messaging system**, Apache-2.0 licensed with **15,000+ GitHub stars** . **Lightweight, high-performance pub/sub** with JetStream for persistence . **Message redelivery and dead letter** . **Best for lightweight messaging with DLQ** .



- **[Apache ActiveMQ](https://github.com/apache/activemq)**  

  **The veteran open-source message broker**, Apache-2.0 licensed . **JMS, AMQP, MQTT, and STOMP** . **Dead letter queues and redelivery policies** . **Best for Java-centric messaging** .



- **[Apache ActiveMQ Artemis](https://github.com/apache/activemq-artemis)**  

  **High-performance messaging broker**, Apache-2.0 licensed . **JMS 2.0 compliant with non-blocking architecture** . **Best for high-performance JMS** .



- **[NSQ](https://github.com/nsqio/nsq)**  

  **Real-time distributed messaging platform**, MIT licensed with **12,000+ GitHub stars** . **Simple, reliable, and scalable** . **Best for simple messaging at scale** .



- **[ZeroMQ](https://github.com/zeromq/libzmq)**  

  **High-performance asynchronous messaging library**, MPL-2.0 licensed . **Embedded networking library** — no broker required . **Best for custom messaging patterns** .



### Task Queues & Job Processing



- **[Celery](https://github.com/celery/celery)**  

  **Distributed task queue for Python**, BSD-3-Clause licensed with **25,000+ GitHub stars** . **Task retries with exponential backoff** . **Dead letter queue** via `task_reject_on_worker_lost` . **Best for Python task queues** .



- **[BullMQ](https://github.com/taskforcesh/bullmq)**  

  **Redis-based queue for Node.js**, MIT licensed with **5,000+ GitHub stars** . **Retry with exponential backoff** . **Dead letter queue** — failed jobs move to DLQ after retries exhausted . **Best for Node.js background jobs** .



- **[Sidekiq](https://github.com/sidekiq/sidekiq)**  

  **Ruby background job processing**, LGPL-3.0 licensed with **13,000+ GitHub stars** . **Retry with backoff** — automatic retries with exponential backoff . **Dead job queue** — failed jobs move to DeadSet . **Best for Ruby background jobs** .



- **[RQ (Redis Queue)](https://github.com/rq/rq)**  

  **Simple Python task queue**, BSD-2-Clause licensed with **9,000+ GitHub stars** . **Retry with backoff** . **Failed queue** — failed jobs move to FailedQueue . **Best for simple Python task queues** .



- **[Beanstalkd](https://github.com/beanstalkd/beanstalkd)**  

  **Simple, fast work queue**, MIT licensed with **6,000+ GitHub stars** . **Delayed jobs and priority queues** . **Best for simple work queues** .



- **[Dramatiq](https://github.com/Bogdanp/dramatiq)**  

  **Fast, reliable Python task processing**, LGPL-3.0 licensed . **Automatic retries and dead letter queues** . **Best for Python task queues** .



- **[Hatchet](https://github.com/hatchet-dev/hatchet)**  

  **Modern task orchestration platform**, MIT licensed . **Durable execution with retries and concurrency limits** . **Best for modern task orchestration** .



### Kubernetes-Native Queuing



- **[KubeMQ](https://github.com/kubemq-io/kubemq-community)**  

  **Kubernetes-native message broker**, Apache-2.0 licensed . **Lightweight and scalable** . **Best for Kubernetes messaging** .



- **[NATS JetStream](https://github.com/nats-io/nats-server)**  

  **Persistence layer for NATS**, Apache-2.0 licensed . **Message redelivery and dead letter** . **Best for Kubernetes-native messaging** .



- **[KEDA](https://github.com/kedacore/keda)**  

  **Kubernetes Event-driven Autoscaling**, Apache-2.0 licensed with **8,000+ GitHub stars** . **Scale workloads based on queue depth** . **Best for event-driven autoscaling** .



### Additional Strong Open-Source Options



- **Redis Pub/Sub** — In-memory pub/sub messaging .

- **Redis Streams** — Persistent log-based messaging .

- **Apache Qpid** — AMQP messaging .

- **HornetQ** — High-performance messaging (merged into Artemis) .

- **Disque** — Distributed job queue .

- **Gearman** — Job server .

- **Kombu** — Messaging library for Python .

- **Laravel Horizon** — Redis queue dashboard for Laravel .

- **WakaQ** — Python task queue with Redis .



**Frameworks for building custom managed message queue solutions**: Combine **RabbitMQ** for reliable message queuing with dead letter exchanges . Use **Apache Kafka** or **Pulsar** for high-throughput event streaming with DLQ patterns . Deploy **Celery** or **Dramatiq** for Python task queues . Choose **BullMQ** for Node.js background jobs with exponential backoff . Integrate **NATS JetStream** for cloud-native messaging . Use **KEDA** for Kubernetes event-driven autoscaling . Note that true managed message queuing with global infrastructure, automatic scaling, and vendor-supported SLAs (SQS, CloudAMQP, Confluent Cloud) remains primarily commercial territory; open-source stacks provide strong queuing, task processing, and event streaming foundations that require integration for complete MQaaS deployments.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Message queue platforms handle critical business data and application state. Self-hosted solutions require proper security hardening, access controls, monitoring, and backup procedures.

- **DLQ configuration is critical** — without DLQ, failed messages are lost or block queues. Configure max retry counts, TTL, and DLQ targets for every queue .

- **Poison messages can block queues** — implement message validation, dead lettering after N retries, and alerting on DLQ depth .

- **Retry with backoff prevents thundering herd** — use exponential backoff with jitter to avoid overwhelming downstream services .

- **License considerations**: RabbitMQ uses MPL-2.0, Kafka uses Apache-2.0, Pulsar uses Apache-2.0, Celery uses BSD-3-Clause, and BullMQ uses MIT. Verify licensing against your use case before committing .

- The open-source ecosystem provides strong queuing, task processing, and event streaming foundations, but **managed infrastructure, global scale, and vendor-supported SLAs** remain primarily commercial offerings.



---



**Made for backend engineers, platform teams, and organizations seeking message queue sovereignty.**  

Let's make managed message queues more open, transparent, and reliable.
