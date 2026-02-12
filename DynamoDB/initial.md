What is difference blw gsi and lsi in dynamodb in simple 

Here’s the simple difference between GSI (Global Secondary Index) and LSI (Local Secondary Index) in DynamoDB 👇

| Feature | GSI (Global Secondary Index) | LSI (Local Secondary Index) |
|--------|--------------------------------|-------------------------------|
| **Partition Key** | Can be different from the base table’s partition key | Must be the same as the base table’s partition key |
| **Sort Key** | Can be different from the base table’s sort key | Must be different from the base table’s sort key |
| **Created** | Can be created anytime (after table creation) | Must be created at the time of table creation |
| **Query Scope** | Can query across all partitions (global) | Queries are limited to the same partition key (local) |
| **Read/Write Capacity** | Has its own read/write capacity (can scale independently) | Shares read/write capacity with the main table |
| **Use Case** | When you want to query data using a completely different key | When you want to query the same partition with different sorting |

🧠 In short:

GSI = Different partition key → global view.

LSI = Same partition key, different sort key → local view.

Would you like a real-world example (like a table of users and queries using GSI and LSI)? It’ll make it much clearer.

