# EvoliaTroops\CustomerApi

All URIs are relative to *https://virtserver.swaggerhub.com/smartgammadev/Evolia/1.0.0-troops*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createCustomer**](CustomerApi.md#createcustomer) | **POST** /customers | Create new customer
[**getCustomerBydId**](CustomerApi.md#getcustomerbydid) | **GET** /customers/{id} | Get customer by id (Evolia ID)
[**updateCustomer**](CustomerApi.md#updatecustomer) | **PUT** /customers/{id} | Update a customer by ID (Evolia ID)

# **createCustomer**
> \EvoliaTroops\Model\CustomerResponseDto createCustomer($body, $authorization)

Create new customer

Create a new customer according to DTO model

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = EvoliaTroops\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EvoliaTroops\SDK\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \EvoliaTroops\Model\CustomerRequestDto(); // \EvoliaTroops\Model\CustomerRequestDto | 
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->createCustomer($body, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->createCustomer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\EvoliaTroops\Model\CustomerRequestDto**](../Model/CustomerRequestDto.md)|  |
 **authorization** | **string**|  |

### Return type

[**\EvoliaTroops\Model\CustomerResponseDto**](../Model/CustomerResponseDto.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCustomerBydId**
> \EvoliaTroops\Model\CustomerResponseDto getCustomerBydId($id, $authorization)

Get customer by id (Evolia ID)

Retrieves the given customer based on its id, if found

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = EvoliaTroops\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EvoliaTroops\SDK\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->getCustomerBydId($id, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->getCustomerBydId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **authorization** | **string**|  |

### Return type

[**\EvoliaTroops\Model\CustomerResponseDto**](../Model/CustomerResponseDto.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateCustomer**
> \EvoliaTroops\Model\CustomerResponseDto updateCustomer($body, $authorization, $id)

Update a customer by ID (Evolia ID)

Update a customer according to DTO model by EvoliaID

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: bearer
    $config = EvoliaTroops\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new EvoliaTroops\SDK\CustomerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \EvoliaTroops\Model\CustomerRequestDto(); // \EvoliaTroops\Model\CustomerRequestDto | 
$authorization = "authorization_example"; // string | 
$id = "id_example"; // string | 

try {
    $result = $apiInstance->updateCustomer($body, $authorization, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerApi->updateCustomer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\EvoliaTroops\Model\CustomerRequestDto**](../Model/CustomerRequestDto.md)|  |
 **authorization** | **string**|  |
 **id** | **string**|  |

### Return type

[**\EvoliaTroops\Model\CustomerResponseDto**](../Model/CustomerResponseDto.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

