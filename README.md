# Distributed-Software-System: Demo-01

The REST APIs are designed to handle structured data in JSON format. It supports CRUD operations with a focus on Create, Read, and Delete functionalities. API is built with robust validation mechanisms and adheres to RESTful principles.

## Features
- Support for CRUD operations (Create, Read, Delete).
- JSON Schema validation for incoming payloads.
- Conditional Read based on data change status.
- Data storage in a key-value store.
- RESTful endpoints with clear URIs and appropriate HTTP status codes.

## Setup
1. Install the dependencies
   
   ```
   npm install
   ```
2. Start the server locally
   
   ```
   npm start
   ```

## Data Model
The data model for this API is defined by the following JSON schema:

```
{
    "planCostShares": {
        "deductible": 2000,
        "_org": "example.com",
        "copay": 23,
        "objectId": "1234vxc2324sdf-501",
        "objectType": "membercostshare"
    },
    "linkedPlanServices": [
        {
            "linkedService": {
                "_org": "example.com",
                "objectId": "1234520xvc30asdf-502",
                "objectType": "service",
                "name": "Yearly physical"
            },
            "planserviceCostShares": {
                "deductible": 10,
                "_org": "example.com",
                "copay": 0,
                "objectId": "1234512xvc1314asdfs-503",
                "objectType": "membercostshare"
            },
            "_org": "example.com",
            "objectId": "27283xvx9asdff-504",
            "objectType": "planservice"
        },
        {
            "linkedService": {
                "_org": "example.com",
                "objectId": "1234520xvc30sfs-505",
                "objectType": "service",
                "name": "well baby"
            },
            "planserviceCostShares": {
                "deductible": 10,
                "_org": "example.com",
                "copay": 175,
                "objectId": "1234512xvc1314sdfsd-506",
                "objectType": "membercostshare"
            },
            "_org": "example.com",
            "objectId": "27283xvx9sdf-507",
            "objectType": "planservice"
        }
    ],
    "_org": "example.com",
    "objectId": "12xvxc345ssdsds-508",
    "objectType": "plan",
    "planType": "inNetwork",
    "creationDate": "12-12-2017"
}
```

## Data Storage
The data is stored in a key-value store using Redis.

## License
This project is licensed under the [MIT License](LICENSE)

## Author
[Siddharth Gargava](mailto:gargavasiddharth@gmail.com)