

# ReceiptSummary

Slim receipt shape for the paginated merchant list endpoint -- omits qr_code_url, items, payment_info, adjustments, warranties, and insights to keep list responses lightweight. Fetch GET /merchant/receipts/{id} for the full detail (QR code included) when a single receipt is opened.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**publicToken** | **String** |  |  |
|**merchantReceiptId** | **String** |  |  [optional] |
|**storeId** | **String** |  |  |
|**organisationId** | **String** |  |  |
|**transactionDate** | **OffsetDateTime** |  |  |
|**totalAmount** | **String** |  |  |
|**currency** | **String** |  |  |
|**itemCount** | **Integer** |  |  |
|**status** | **String** |  |  |
|**accessCount** | **Integer** |  |  |
|**receiptUrl** | **String** |  |  |
|**createdAt** | **OffsetDateTime** |  |  |



