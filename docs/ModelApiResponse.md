

# ModelApiResponse

Standard API response format.  All API responses should follow this format for consistency. The 'data' field contains the response payload, while 'error' is populated when an error occurs. Pagination is included for list endpoints.  Example:     Success response:     {         \"data\": {\"id\": \"123\", \"name\": \"Logo\"},         \"pagination\": {\"page\": 1, \"limit\": 10, \"total\": 100, \"has_next\": true}     }      Error response:     {         \"error\": {             \"code\": \"VALIDATION_ERROR\",             \"message\": \"File size exceeds 5MB limit\",             \"details\": {\"max_size\": \"5242880\"}         }     }

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**data** | **Map&lt;String, Object&gt;** | Response payload data |  [optional] |
|**error** | [**ErrorDetail**](ErrorDetail.md) | Error information |  [optional] |
|**pagination** | [**PaginationInfo**](PaginationInfo.md) | Pagination information for list responses |  [optional] |



