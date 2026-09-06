

# ReceiptCreate

Receipt creation request.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**merchantReceiptId** | **String** |  |  [optional] |
|**dedupeKey** | **String** |  |  [optional] |
|**barcode** | [**Barcode**](Barcode.md) |  |  [optional] |
|**storeId** | **String** |  |  [optional] |
|**transactionDate** | **OffsetDateTime** |  |  |
|**orderNumber** | **String** |  |  [optional] |
|**cashier** | **String** |  |  [optional] |
|**items** | [**List&lt;ReceiptItemCreate&gt;**](ReceiptItemCreate.md) |  |  |
|**subtotal** | **String** |  |  |
|**taxAmount** | **String** |  |  |
|**discountAmount** | **String** |  |  [optional] |
|**tipAmount** | **String** |  |  [optional] |
|**totalAmount** | **String** |  |  |
|**currency** | **String** |  |  |
|**paymentInfo** | [**List&lt;PaymentInfoCreate&gt;**](PaymentInfoCreate.md) |  |  |
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
|**qrExpiryMinutes** | **Integer** |  |  [optional] |



