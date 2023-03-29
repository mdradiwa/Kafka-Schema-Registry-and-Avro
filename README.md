# Kafka Schema Registry and Avro
Creating **Avro Producer** and **Avro Consumer** using the bitcoin_price_Training dataset and load it to Google BigQuery.
## Tech Stack
- Avro
- Python
- Java
- Confluent Kafka
- Docker
## Setup
1. Run the Confluent Kafka via `docker compose up`.
2. Create the Avro schema.
3. Clean the **bitcoin_price_Training** dataset. The result of the cleaned dataset are attached in the **data** folder in this repository.
4. Run the producer via python in the directory that store the file with the following result in the terminal if its successful,
   ![producer avro](https://user-images.githubusercontent.com/124119569/228620407-5230180f-1747-4819-bec3-6c6bdc4d4372.jpg)

5. Run the consumer via python in the directory that store the file. We can check the data via Big Query if its already loaded or not,
   ![bitcoin bigquery](https://user-images.githubusercontent.com/124119569/228621016-ace86901-81ac-42ac-b564-754b65ead0c0.jpg)
   
**note:** We should create google credential first so we can load the dataset into Big Query.

6. We can monitor what happen via Confluent Kafka,
   - The topic we deployed (**practice_bitcoin_price_Training**),
![Screenshot (645)](https://user-images.githubusercontent.com/124119569/228622137-82194eb7-d479-4d15-80af-b3ba2399986d.png)

   - The consumer we deployed (**practice.bitcoin.avro.consumer.2**),
![Screenshot (644)](https://user-images.githubusercontent.com/124119569/228622165-5546d840-3408-4239-ad60-5ce52811d86e.png)

   - The incoming message from producer,
![Screenshot (643)](https://user-images.githubusercontent.com/124119569/228622792-6c9c6ceb-e9aa-4419-a0f9-1adfecedf522.png)

   - The schema,
![Screenshot (642)](https://user-images.githubusercontent.com/124119569/228622988-fc74eb8f-699c-4e24-ba7c-9d765f55f32d.png)

  
