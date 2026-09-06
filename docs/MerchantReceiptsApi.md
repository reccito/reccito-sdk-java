# MerchantReceiptsApi

All URIs are relative to *https://api.reccito.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createReceipt**](MerchantReceiptsApi.md#createReceipt) | **POST** /api/v1/merchant/receipts | Create Receipt |
| [**getReceipt**](MerchantReceiptsApi.md#getReceipt) | **GET** /api/v1/merchant/receipts/{receipt_id} | Get Receipt |
| [**listReceipts**](MerchantReceiptsApi.md#listReceipts) | **GET** /api/v1/merchant/receipts | List Receipts |
| [**refreshReceiptQr**](MerchantReceiptsApi.md#refreshReceiptQr) | **PUT** /api/v1/merchant/receipts/{receipt_id}/refresh-qr | Refresh Qr Code |


<a id="createReceipt"></a>
# **createReceipt**
> ReceiptImmediateResponse createReceipt(receiptCreate)

Create Receipt

Create a new receipt. Synchronous: the receipt is durably persisted before this returns (see ReceiptService.create_receipt_synchronously). A retry with the same dedupe_key returns the original receipt with 200, not an error (idempotent replay, Stripe-style).

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantReceiptsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantReceiptsApi apiInstance = new MerchantReceiptsApi(defaultClient);
    ReceiptCreate receiptCreate = new ReceiptCreate(); // ReceiptCreate | 
    try {
      ReceiptImmediateResponse result = apiInstance.createReceipt(receiptCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantReceiptsApi#createReceipt");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptCreate** | [**ReceiptCreate**](ReceiptCreate.md)|  | |

### Return type

[**ReceiptImmediateResponse**](ReceiptImmediateResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successful Response |  -  |
| **200** | Idempotent replay: a receipt with this organisation + dedupe_key already existed. Returns the original receipt unchanged, not an error. |  -  |
| **422** | Validation Error |  -  |

<a id="getReceipt"></a>
# **getReceipt**
> MerchantReceiptResponse getReceipt(receiptId)

Get Receipt

Get receipt by ID.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantReceiptsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantReceiptsApi apiInstance = new MerchantReceiptsApi(defaultClient);
    String receiptId = "receiptId_example"; // String | 
    try {
      MerchantReceiptResponse result = apiInstance.getReceipt(receiptId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantReceiptsApi#getReceipt");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptId** | **String**|  | |

### Return type

[**MerchantReceiptResponse**](MerchantReceiptResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="listReceipts"></a>
# **listReceipts**
> ReceiptListResponse listReceipts(page, limit, storeId, status, search, sortBy, sortOrder)

List Receipts

List receipts with filters and pagination.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantReceiptsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantReceiptsApi apiInstance = new MerchantReceiptsApi(defaultClient);
    Integer page = 1; // Integer | 
    Integer limit = 50; // Integer | 
    String storeId = "storeId_example"; // String | 
    String status = "status_example"; // String | 
    String search = "search_example"; // String | 
    String sortBy = "created_at"; // String | 
    String sortOrder = "desc"; // String | 
    try {
      ReceiptListResponse result = apiInstance.listReceipts(page, limit, storeId, status, search, sortBy, sortOrder);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantReceiptsApi#listReceipts");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **page** | **Integer**|  | [optional] [default to 1] |
| **limit** | **Integer**|  | [optional] [default to 50] |
| **storeId** | **String**|  | [optional] |
| **status** | **String**|  | [optional] |
| **search** | **String**|  | [optional] |
| **sortBy** | **String**|  | [optional] [default to created_at] |
| **sortOrder** | **String**|  | [optional] [default to desc] |

### Return type

[**ReceiptListResponse**](ReceiptListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="refreshReceiptQr"></a>
# **refreshReceiptQr**
> QRRefreshResponse refreshReceiptQr(receiptId)

Refresh Qr Code

Refresh QR code for a receipt.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantReceiptsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantReceiptsApi apiInstance = new MerchantReceiptsApi(defaultClient);
    String receiptId = "receiptId_example"; // String | 
    try {
      QRRefreshResponse result = apiInstance.refreshReceiptQr(receiptId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantReceiptsApi#refreshReceiptQr");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **receiptId** | **String**|  | |

### Return type

[**QRRefreshResponse**](QRRefreshResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

