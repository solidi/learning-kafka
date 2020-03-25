# Learning Kafka

## Philosophy

- ETL is dead, long live streaming.

## Use Cases

- Analytics
- Log Collections
- Stream processing

## Core Concepts

- Invited by LinkedIn, and is now an apache open source project.
- A loosely coupled system, message system as a bus.
- Producer / Consumer model
    - Producer sends change/events
        - Updates to customer info
        - New orders
        - Page views
        - Scanning products
        - Publishes data to topics
        - Uses Parititoner
        - Replication complete before read
        - Focus on throughput
        - Config
            - Messaging durability (how it responds)
            - Ordering/retry
            - Batching and compression
            - Queuing limits
        - Producer API
    - Consumer is more complex than producers
        - Read data from topics
        - Organized into groups
            - GroupID
            - Session timeout
            - Heartbeat (for zookeeper)
            - Autocommit
        - Partitions divided among them
        - Rebalanced / Zookeeper > Broker coordinater
- Connectors are DB's, usually.
- Stream processors that connect to inspect.
- The log is the source of truth.
- Consistent messages and tranactions.
- Contains brokers based by topic, and partitions of those topics.
- Topics
    - Category/Feed
    - Partitioned (Lead Parititon is 0)
    - Immutable
- Broker
    - Logical (buckets)
    - Many Topics
    - Resilient
- Focus is on latency and thruput. 
    - Minimum 32gb ram, 24 cpu cores, numerous drives.


## Questions

- Apps that push data into Kafka are known as producers.
- LinkedIn created Kafka.
- The log is a series of changes to a specific entity in Kafka.
- Historical tracking changes is key benefit of using Kafka.
- Inside the Kafka cluster, topics are partitioned across brokers.
- Producers perform writes to a topic.
- Partitioners decide where to write data from the producers.
- Consumers are organized by consuer groups.
- Deleting a topic is an operational task that requires special settings to be applied.
- Another broker becomes the primary  partition of a topic if the broker fails.

## Resources

1. [The Log](https://goo.gl/emw4M2)
1. [kafka-monitor](https://github.com/linkedin/kafka-monitor)
1. [confluent.io](https://www.confluent.io/)
1. [Cloudera](https://www.cloudera.com/)
1. [HortonWorks](https://hortonworks.com/)
1. [AWS Kinesis](https://aws.amazon.com/kinesis)
