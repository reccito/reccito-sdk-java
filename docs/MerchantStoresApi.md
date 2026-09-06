# MerchantStoresApi

All URIs are relative to *https://api.reccito.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createStore**](MerchantStoresApi.md#createStore) | **POST** /api/v1/merchant/stores | Create Store |
| [**getStore**](MerchantStoresApi.md#getStore) | **GET** /api/v1/merchant/stores/{store_id} | Get Store |
| [**getStoreStats**](MerchantStoresApi.md#getStoreStats) | **GET** /api/v1/merchant/stores/{store_id}/stats | Get Store Stats |
| [**listStores**](MerchantStoresApi.md#listStores) | **GET** /api/v1/merchant/stores | List Stores |
| [**updateStore**](MerchantStoresApi.md#updateStore) | **PUT** /api/v1/merchant/stores/{store_id} | Update Store |


<a id="createStore"></a>
# **createStore**
> StoreResponse createStore(storeCreate)

Create Store

Create a new store for the organisation.  **Authentication:** Required (Organisation bearer token)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantStoresApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantStoresApi apiInstance = new MerchantStoresApi(defaultClient);
    StoreCreate storeCreate = new StoreCreate(); // StoreCreate | 
    try {
      StoreResponse result = apiInstance.createStore(storeCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantStoresApi#createStore");
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
| **storeCreate** | [**StoreCreate**](StoreCreate.md)|  | |

### Return type

[**StoreResponse**](StoreResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="getStore"></a>
# **getStore**
> StoreResponse getStore(storeId)

Get Store

Get a specific store by ID.  **Authentication:** Required (Organisation bearer token)  **Path Parameters:** - &#x60;store_id&#x60;: UUID of the store

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantStoresApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantStoresApi apiInstance = new MerchantStoresApi(defaultClient);
    UUID storeId = UUID.randomUUID(); // UUID | 
    try {
      StoreResponse result = apiInstance.getStore(storeId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantStoresApi#getStore");
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
| **storeId** | **UUID**|  | |

### Return type

[**StoreResponse**](StoreResponse.md)

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

<a id="getStoreStats"></a>
# **getStoreStats**
> StoreStatsResponse getStoreStats(storeId)

Get Store Stats

Get statistics for a store.  **Authentication:** Required (Organisation bearer token)  **Path Parameters:** - &#x60;store_id&#x60;: UUID of the store

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantStoresApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantStoresApi apiInstance = new MerchantStoresApi(defaultClient);
    UUID storeId = UUID.randomUUID(); // UUID | 
    try {
      StoreStatsResponse result = apiInstance.getStoreStats(storeId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantStoresApi#getStoreStats");
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
| **storeId** | **UUID**|  | |

### Return type

[**StoreStatsResponse**](StoreStatsResponse.md)

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

<a id="listStores"></a>
# **listStores**
> StoreListResponse listStores(skip, limit, isActive, q)

List Stores

List all stores for the organisation.  **Authentication:** Required (Organisation bearer token)  **Query Parameters:** - &#x60;skip&#x60;: Number of stores to skip (default: 0) - &#x60;limit&#x60;: Number of stores to return (default: 100, max: 1000) - &#x60;is_active&#x60;: Filter by active status (optional) - &#x60;q&#x60;: Search by store name/code/city/email/phone (optional)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantStoresApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantStoresApi apiInstance = new MerchantStoresApi(defaultClient);
    Integer skip = 0; // Integer | 
    Integer limit = 100; // Integer | 
    Boolean isActive = true; // Boolean | 
    String q = "q_example"; // String | 
    try {
      StoreListResponse result = apiInstance.listStores(skip, limit, isActive, q);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantStoresApi#listStores");
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
| **skip** | **Integer**|  | [optional] [default to 0] |
| **limit** | **Integer**|  | [optional] [default to 100] |
| **isActive** | **Boolean**|  | [optional] |
| **q** | **String**|  | [optional] |

### Return type

[**StoreListResponse**](StoreListResponse.md)

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

<a id="updateStore"></a>
# **updateStore**
> StoreResponse updateStore(storeId, storeUpdate)

Update Store

Update a store.  **Authentication:** Required (Organisation bearer token)  **Path Parameters:** - &#x60;store_id&#x60;: UUID of the store  **Request Body:** Updated store fields (all optional)

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantStoresApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantStoresApi apiInstance = new MerchantStoresApi(defaultClient);
    UUID storeId = UUID.randomUUID(); // UUID | 
    StoreUpdate storeUpdate = new StoreUpdate(); // StoreUpdate | 
    try {
      StoreResponse result = apiInstance.updateStore(storeId, storeUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantStoresApi#updateStore");
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
| **storeId** | **UUID**|  | |
| **storeUpdate** | [**StoreUpdate**](StoreUpdate.md)|  | |

### Return type

[**StoreResponse**](StoreResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

