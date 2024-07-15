# BckbnPay::ChargesApi

All URIs are relative to *https://pay.bckbn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**charges_get**](ChargesApi.md#charges_get) | **GET** /charges | List all charges |
| [**charges_id_get**](ChargesApi.md#charges_id_get) | **GET** /charges/{id} | Retrieve a charge |
| [**charges_post**](ChargesApi.md#charges_post) | **POST** /charges | Create a charge |


## charges_get

> <ChargesGet200Response> charges_get(x_api_version, content_type)

List all charges

### Examples

```ruby
require 'time'
require 'bckbn_pay'
# setup authorization
BckbnPay.configure do |config|
  # Configure Bearer authorization (access_token): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = BckbnPay::ChargesApi.new
x_api_version = 'x_api_version_example' # String | 
content_type = 'application/json' # String | 

begin
  # List all charges
  result = api_instance.charges_get(x_api_version, content_type)
  p result
rescue BckbnPay::ApiError => e
  puts "Error when calling ChargesApi->charges_get: #{e}"
end
```

#### Using the charges_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ChargesGet200Response>, Integer, Hash)> charges_get_with_http_info(x_api_version, content_type)

```ruby
begin
  # List all charges
  data, status_code, headers = api_instance.charges_get_with_http_info(x_api_version, content_type)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ChargesGet200Response>
rescue BckbnPay::ApiError => e
  puts "Error when calling ChargesApi->charges_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **x_api_version** | **String** |  |  |
| **content_type** | **String** |  |  |

### Return type

[**ChargesGet200Response**](ChargesGet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## charges_id_get

> <Charge> charges_id_get(x_api_version, content_type, id)

Retrieve a charge

### Examples

```ruby
require 'time'
require 'bckbn_pay'
# setup authorization
BckbnPay.configure do |config|
  # Configure Bearer authorization (access_token): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = BckbnPay::ChargesApi.new
x_api_version = 'x_api_version_example' # String | 
content_type = 'application/json' # String | 
id = 'id_example' # String | 

begin
  # Retrieve a charge
  result = api_instance.charges_id_get(x_api_version, content_type, id)
  p result
rescue BckbnPay::ApiError => e
  puts "Error when calling ChargesApi->charges_id_get: #{e}"
end
```

#### Using the charges_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Charge>, Integer, Hash)> charges_id_get_with_http_info(x_api_version, content_type, id)

```ruby
begin
  # Retrieve a charge
  data, status_code, headers = api_instance.charges_id_get_with_http_info(x_api_version, content_type, id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Charge>
rescue BckbnPay::ApiError => e
  puts "Error when calling ChargesApi->charges_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **x_api_version** | **String** |  |  |
| **content_type** | **String** |  |  |
| **id** | **String** |  |  |

### Return type

[**Charge**](Charge.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## charges_post

> <Charge> charges_post(x_api_version, content_type, charges_post_request)

Create a charge

### Examples

```ruby
require 'time'
require 'bckbn_pay'
# setup authorization
BckbnPay.configure do |config|
  # Configure Bearer authorization (access_token): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = BckbnPay::ChargesApi.new
x_api_version = 'x_api_version_example' # String | 
content_type = 'application/json' # String | 
charges_post_request = BckbnPay::ChargesPostRequest.new # ChargesPostRequest | 

begin
  # Create a charge
  result = api_instance.charges_post(x_api_version, content_type, charges_post_request)
  p result
rescue BckbnPay::ApiError => e
  puts "Error when calling ChargesApi->charges_post: #{e}"
end
```

#### Using the charges_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Charge>, Integer, Hash)> charges_post_with_http_info(x_api_version, content_type, charges_post_request)

```ruby
begin
  # Create a charge
  data, status_code, headers = api_instance.charges_post_with_http_info(x_api_version, content_type, charges_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Charge>
rescue BckbnPay::ApiError => e
  puts "Error when calling ChargesApi->charges_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **x_api_version** | **String** |  |  |
| **content_type** | **String** |  |  |
| **charges_post_request** | [**ChargesPostRequest**](ChargesPostRequest.md) |  |  |

### Return type

[**Charge**](Charge.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json
