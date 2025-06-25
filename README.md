
# Azure Billing Record Archival and Retrieval System

This project provides a solution to archive old billing records from Azure Cosmos DB to Azure Blob Storage, reducing storage costs while maintaining data availability.

## Components

- `archive_function`: Azure Function to move records older than 90 days from Cosmos DB to Blob Storage.
- `proxy_service`: Read proxy to serve data from Cosmos DB or Blob Storage seamlessly.

## Deployment

1. Configure environment variables:
   - COSMOS_ENDPOINT, COSMOS_KEY, COSMOS_DB, COSMOS_CONTAINER
   - BLOB_CONN_STR, BLOB_CONTAINER

2. Deploy Azure Function with Timer Trigger to run daily.

3. Integrate `read_proxy.py` in your API service for read operations.

## License

MIT
