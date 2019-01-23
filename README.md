## Pending Cancellation
The extension shows  whether a lot is pending for cancellation.
# Overview
The fields introduced by this extension are:
- `tender/pendingCancellation` - Yes or No field showing  whether a lot is pending for cancellation. 
It should be boolean value.
- `lots/pendingCancellation` - Yes or No field showing  whether a lot is pending for cancellation.
It should be boolean value.
# Examples
The following extract illustrates these properties in use within the 
`tender` and `lots` blocks.
```
{
    "tender": {
        "id": "ocds-213czf-lots-00001-01-tender",
        "title": "Architecture and engineering services",
        "description": "The authority is seeking support to construct a new public building.",
        "procurementMethod": "open",
        "status": "active",
        "pendingCancellation": true,
        "items": [
          {
            "id": "0001",
            "description": "Architectural advice",
            "classification": {
              "scheme": "CPV",
              "id": "71210000",
              "description": "Advisory architectural services"
            },
            "relatedLot": "lot-1"
          },
          {
            "id": "0002",
            "description": "Architectural design",
            "classification": {
              "scheme": "CPV",
              "id": "71220000",
              "description": "Architectural design services"
            },
            "relatedLot": "lot-1"
          },
          {
            "id": "0003",
            "description": "Civil engineering consultant",
            "classification": {
              "scheme": "CPV",
              "id": "71311000",
              "description": "Civil engineering consultancy services"
            },
            "relatedLot": "lot-2"
          },
          {
            "id": "0004",
            "description": "Structural engineering services",
            "classification": {
              "scheme": "CPV",
              "id": "71312000",
              "description": "Structural engineering consultancy services"
            },
            "relatedLot": "lot-1"
          }
        ],
        "value": {
          "amount": 1200000,
          "currency": "GBP"
        },
        "lots": [
          {
            "id": "lot-1",
            "title": "Architectural services",
            "description": "For architectural services delivered in the project",
            "status": "active",
            "value": {
              "currency": "GBP",
              "amount": 200000
            },
            "pendingCancellation": true
          }
        ]
    }
}
```