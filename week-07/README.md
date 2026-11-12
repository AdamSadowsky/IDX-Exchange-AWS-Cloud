Created an AWS Lambda function named get-property using Python 3.12.

The function retrieves property information from a DynamoDB table named Properties using the listing ID.

Configured API Gateway with the following route:

GET /properties/{id}

The Lambda function uses an IAM execution role with a custom DynamoDB GetItem permission.

Request Flow

```

Client (curl)
    |
    | HTTP GET /properties/R100234
    v
API Gateway
    |
    | Invokes Lambda
    v
Lambda (get-property)
    |
    | Queries by L_ListingID
    v
DynamoDB (Properties)
    |
    | Returns property record
    v
Lambda
    |
    | Returns JSON response
    v
API Gateway
    |
    v
Client

```