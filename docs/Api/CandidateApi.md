# EvoliaTroops\CandidateApi

All URIs are relative to *https://virtserver.swaggerhub.com/smartgammadev/Evolia/1.0.0-troops*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create**](CandidateApi.md#create) | **POST** /candidates | Create new candidate
[**getcandidateByEmail**](CandidateApi.md#getcandidatebyemail) | **GET** /candidates | Get candidate by email
[**getcandidateBydId**](CandidateApi.md#getcandidatebydid) | **GET** /candidates/{id} | Get candidate by id (Evolia ID)
[**update**](CandidateApi.md#update) | **PUT** /candidates/{id} | Update a candidate by ID (Evolia ID)

# **create**
> \EvoliaTroops\Model\CandidateResponseDto create($body, $authorization)

Create new candidate

Create a new candidate according to DTO model

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = EvoliaTroops\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EvoliaTroops\SDK\CandidateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \EvoliaTroops\Model\CandidateRequestDto(); // \EvoliaTroops\Model\CandidateRequestDto | 
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->create($body, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CandidateApi->create: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\EvoliaTroops\Model\CandidateRequestDto**](../Model/CandidateRequestDto.md)|  |
 **authorization** | **string**|  |

### Return type

[**\EvoliaTroops\Model\CandidateResponseDto**](../Model/CandidateResponseDto.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getcandidateByEmail**
> \EvoliaTroops\Model\CandidateResponseDto getcandidateByEmail($email, $authorization)

Get candidate by email

Retrieves the given candidate based on its email, if found

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = EvoliaTroops\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EvoliaTroops\SDK\CandidateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email = "email_example"; // string | 
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->getcandidateByEmail($email, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CandidateApi->getcandidateByEmail: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **string**|  |
 **authorization** | **string**|  |

### Return type

[**\EvoliaTroops\Model\CandidateResponseDto**](../Model/CandidateResponseDto.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getcandidateBydId**
> \EvoliaTroops\Model\CandidateResponseDto getcandidateBydId($id, $authorization)

Get candidate by id (Evolia ID)

Retrieves the given candidate based on its id, if found

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = EvoliaTroops\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EvoliaTroops\SDK\CandidateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->getcandidateBydId($id, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CandidateApi->getcandidateBydId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **authorization** | **string**|  |

### Return type

[**\EvoliaTroops\Model\CandidateResponseDto**](../Model/CandidateResponseDto.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **update**
> \EvoliaTroops\Model\CandidateResponseDto update($body, $authorization, $id)

Update a candidate by ID (Evolia ID)

Update a candidate from his Evolia ID. This route will update and replace all the fields in the candidate model (Not a PATCH route)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = EvoliaTroops\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EvoliaTroops\SDK\CandidateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \EvoliaTroops\Model\CandidateRequestDto(); // \EvoliaTroops\Model\CandidateRequestDto | 
$authorization = "authorization_example"; // string | 
$id = "id_example"; // string | 

try {
    $result = $apiInstance->update($body, $authorization, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CandidateApi->update: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\EvoliaTroops\Model\CandidateRequestDto**](../Model/CandidateRequestDto.md)|  |
 **authorization** | **string**|  |
 **id** | **string**|  |

### Return type

[**\EvoliaTroops\Model\CandidateResponseDto**](../Model/CandidateResponseDto.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

