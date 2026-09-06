# MerchantAssetsApi

All URIs are relative to *https://api.reccito.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listOrganisationAssets**](MerchantAssetsApi.md#listOrganisationAssets) | **GET** /api/v1/merchant/assets/list | List organisation assets |
| [**uploadOrganisationBanner**](MerchantAssetsApi.md#uploadOrganisationBanner) | **POST** /api/v1/merchant/assets/upload/banner | Upload organisation banner |
| [**uploadOrganisationLogo**](MerchantAssetsApi.md#uploadOrganisationLogo) | **POST** /api/v1/merchant/assets/upload/logo | Upload organisation logo |
| [**uploadStoreLogo**](MerchantAssetsApi.md#uploadStoreLogo) | **POST** /api/v1/merchant/assets/upload/store/logo | Upload store logo |


<a id="listOrganisationAssets"></a>
# **listOrganisationAssets**
> ModelApiResponse listOrganisationAssets(assetType)

List organisation assets

List all branding assets uploaded for the organisation.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantAssetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantAssetsApi apiInstance = new MerchantAssetsApi(defaultClient);
    String assetType = "assetType_example"; // String | 
    try {
      ModelApiResponse result = apiInstance.listOrganisationAssets(assetType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantAssetsApi#listOrganisationAssets");
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
| **assetType** | **String**|  | [optional] |

### Return type

[**ModelApiResponse**](ModelApiResponse.md)

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

<a id="uploadOrganisationBanner"></a>
# **uploadOrganisationBanner**
> ModelApiResponse uploadOrganisationBanner(_file)

Upload organisation banner

Upload a banner file for the organisation. Supported formats: JPEG, PNG, WebP. Max 5MB.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantAssetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantAssetsApi apiInstance = new MerchantAssetsApi(defaultClient);
    File _file = new File("/path/to/file"); // File | Banner file to upload
    try {
      ModelApiResponse result = apiInstance.uploadOrganisationBanner(_file);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantAssetsApi#uploadOrganisationBanner");
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
| **_file** | **File**| Banner file to upload | |

### Return type

[**ModelApiResponse**](ModelApiResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="uploadOrganisationLogo"></a>
# **uploadOrganisationLogo**
> ModelApiResponse uploadOrganisationLogo(_file)

Upload organisation logo

Upload a logo file for the organisation. Supported formats: JPEG, PNG, WebP, SVG. Max 5MB.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantAssetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantAssetsApi apiInstance = new MerchantAssetsApi(defaultClient);
    File _file = new File("/path/to/file"); // File | Logo file to upload
    try {
      ModelApiResponse result = apiInstance.uploadOrganisationLogo(_file);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantAssetsApi#uploadOrganisationLogo");
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
| **_file** | **File**| Logo file to upload | |

### Return type

[**ModelApiResponse**](ModelApiResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="uploadStoreLogo"></a>
# **uploadStoreLogo**
> ModelApiResponse uploadStoreLogo(storeId, _file)

Upload store logo

Upload a logo file for a specific store. Supported formats: JPEG, PNG, WebP, SVG. Max 5MB.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.MerchantAssetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.reccito.com");
    
    // Configure HTTP bearer authorization: ApiKeyAuth
    HttpBearerAuth ApiKeyAuth = (HttpBearerAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setBearerToken("BEARER TOKEN");

    MerchantAssetsApi apiInstance = new MerchantAssetsApi(defaultClient);
    String storeId = "storeId_example"; // String | 
    File _file = new File("/path/to/file"); // File | Store logo file to upload
    try {
      ModelApiResponse result = apiInstance.uploadStoreLogo(storeId, _file);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MerchantAssetsApi#uploadStoreLogo");
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
| **storeId** | **String**|  | |
| **_file** | **File**| Store logo file to upload | |

### Return type

[**ModelApiResponse**](ModelApiResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

