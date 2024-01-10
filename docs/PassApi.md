# SwaggerClient::PassApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_or_update_pass**](PassApi.md#create_or_update_pass) | **POST** /pass | This method creates or (if the pass id already exists) updates a pass, so you don&#39;t have to track ids and creation status of your passes.
[**delete_pass**](PassApi.md#delete_pass) | **DELETE** /pass | Delete pass by pass id.
[**get_pass**](PassApi.md#get_pass) | **GET** /pass | Get pass information by pass id.
[**pass_list**](PassApi.md#pass_list) | **GET** /pass/list | Retrieve the list of active pass ids for a given pass type.
[**pass_sync**](PassApi.md#pass_sync) | **POST** /pass/sync | Send updates to all active passes for a given pass type.


# **create_or_update_pass**
> create_or_update_pass(pass_type_id, opts)

This method creates or (if the pass id already exists) updates a pass, so you don't have to track ids and creation status of your passes.

This method creates or (if the pass id already exists) updates a pass, so you don't have to track ids and creation status of your passes.

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::PassApi.new

pass_type_id = nil # Object | your pass type id, for example P963493 (Urban Fitness)

opts = { 
  pass_id: nil # Object | id of the pass (provided by you when creating the pass or automatically set by passmeister)
}

begin
  #This method creates or (if the pass id already exists) updates a pass, so you don't have to track ids and creation status of your passes.
  api_instance.create_or_update_pass(pass_type_id, opts)
rescue SwaggerClient::ApiError => e
  puts "Exception when calling PassApi->create_or_update_pass: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pass_type_id** | [**Object**](.md)| your pass type id, for example P963493 (Urban Fitness) | 
 **pass_id** | [**Object**](.md)| id of the pass (provided by you when creating the pass or automatically set by passmeister) | [optional] 

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **delete_pass**
> delete_pass(pass_type_id, pass_id)

Delete pass by pass id.

Delete pass by pass id.

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::PassApi.new

pass_type_id = nil # Object | your pass type id, for example P963493 (Urban Fitness)

pass_id = nil # Object | id of the pass


begin
  #Delete pass by pass id.
  api_instance.delete_pass(pass_type_id, pass_id)
rescue SwaggerClient::ApiError => e
  puts "Exception when calling PassApi->delete_pass: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pass_type_id** | [**Object**](.md)| your pass type id, for example P963493 (Urban Fitness) | 
 **pass_id** | [**Object**](.md)| id of the pass | 

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **get_pass**
> get_pass(pass_type_id, pass_id)

Get pass information by pass id.

Get pass information by pass id.

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::PassApi.new

pass_type_id = nil # Object | your pass type id, for example P963493 (Urban Fitness)

pass_id = nil # Object | id of the pass


begin
  #Get pass information by pass id.
  api_instance.get_pass(pass_type_id, pass_id)
rescue SwaggerClient::ApiError => e
  puts "Exception when calling PassApi->get_pass: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pass_type_id** | [**Object**](.md)| your pass type id, for example P963493 (Urban Fitness) | 
 **pass_id** | [**Object**](.md)| id of the pass | 

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **pass_list**
> pass_list(pass_type_id, opts)

Retrieve the list of active pass ids for a given pass type.

Retrieve the list of active pass ids for a given pass type.

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::PassApi.new

pass_type_id = nil # Object | your pass type id, for example P963493 (Urban Fitness)

opts = { 
  page: nil, # Object | 
  limit: nil # Object | 
}

begin
  #Retrieve the list of active pass ids for a given pass type.
  api_instance.pass_list(pass_type_id, opts)
rescue SwaggerClient::ApiError => e
  puts "Exception when calling PassApi->pass_list: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pass_type_id** | [**Object**](.md)| your pass type id, for example P963493 (Urban Fitness) | 
 **page** | [**Object**](.md)|  | [optional] 
 **limit** | [**Object**](.md)|  | [optional] 

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **pass_sync**
> pass_sync(pass_type_id)

Send updates to all active passes for a given pass type.

For example: you changed the pass type layout and now you want to update all installed passes. (The API call only confirms the scheduling of the updates, actual updating of passes on your customers devices can take a while.)

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::PassApi.new

pass_type_id = nil # Object | your pass type id, for example P963493 (Urban Fitness)


begin
  #Send updates to all active passes for a given pass type.
  api_instance.pass_sync(pass_type_id)
rescue SwaggerClient::ApiError => e
  puts "Exception when calling PassApi->pass_sync: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pass_type_id** | [**Object**](.md)| your pass type id, for example P963493 (Urban Fitness) | 

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



