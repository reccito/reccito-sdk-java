

# MerchantReceiptResponse

Receipt response for the merchant audience (dashboard, merchant API keys).  Excludes customer-upload-pipeline fields (uploaded_file_url, file_size, file_type, original_filename, extraction_status/confidence/method/ completed_at, receipt_source, uploaded_by_customer_id), which are always null for merchant-issued receipts and belong to the separate customer-audience response shape instead.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**publicToken** | **String** |  |  |
|**barcode** | [**Barcode**](Barcode.md) |  |  [optional] |
|**merchantReceiptId** | **String** |  |  [optional] |
|**merchantName** | **String** |  |  [optional] |
|**merchantLogo** | **String** |  |  [optional] |
|**storeId** | **String** |  |  |
|**organisationId** | **String** |  |  |
|**transactionDate** | **OffsetDateTime** |  |  |
|**orderNumber** | **String** |  |  [optional] |
|**cashier** | **String** |  |  [optional] |
|**items** | [**List&lt;ReceiptItemResponse&gt;**](ReceiptItemResponse.md) |  |  |
|**subtotal** | **String** |  |  |
|**taxAmount** | **String** |  |  |
|**discountAmount** | **String** |  |  |
|**tipAmount** | **String** |  |  |
|**totalAmount** | **String** |  |  |
|**currency** | **String** |  |  |
|**paymentInfo** | [**List&lt;PaymentInfoResponse&gt;**](PaymentInfoResponse.md) |  |  |
|**qrCodeUrl** | **String** |  |  |
|**qrToken** | **String** |  |  |
|**qrExpiresAt** | **OffsetDateTime** |  |  |
|**receiptUrl** | **String** |  |  |
|**pdfUrl** | **String** |  |  [optional] |
|**notes** | **String** |  |  [optional] |
|**returnPolicy** | **String** |  |  [optional] |
|**offers** | **List&lt;String&gt;** |  |  [optional] |
|**offerPolicies** | [**List&lt;OfferPolicyInfo&gt;**](OfferPolicyInfo.md) |  |  [optional] |
|**feedbackUrl** | **String** |  |  [optional] |
|**loyaltyInfo** | **String** |  |  [optional] |
|**merchantDetails** | [**MerchantDetails**](MerchantDetails.md) |  |  [optional] |
|**adjustments** | [**List&lt;ReceiptAdjustment&gt;**](ReceiptAdjustment.md) |  |  [optional] |
|**transactionReferences** | [**List&lt;TransactionReference&gt;**](TransactionReference.md) |  |  [optional] |
|**warranties** | [**List&lt;WarrantyInfo&gt;**](WarrantyInfo.md) |  |  [optional] |
|**insights** | [**ReceiptInsights**](ReceiptInsights.md) |  |  [optional] |
|**returnInsights** | [**ReturnInsights**](ReturnInsights.md) |  |  [optional] |
|**accessCount** | **Integer** |  |  |
|**lastAccessed** | **OffsetDateTime** |  |  [optional] |
|**status** | **String** |  |  |
|**expiresAt** | **OffsetDateTime** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  |
|**updatedAt** | **OffsetDateTime** |  |  |



