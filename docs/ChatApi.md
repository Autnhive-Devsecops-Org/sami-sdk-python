# sami_firewall_client.ChatApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**adapter_chat**](ChatApi.md#adapter_chat) | **POST** /ai-firewall/firewall/v1/prompt/text | Firewall text chat endpoint


# **adapter_chat**
> Dict[str, object] adapter_chat(request_body)

Firewall text chat endpoint

### Example


```python
import sami_firewall_client
from sami_firewall_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = sami_firewall_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with sami_firewall_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sami_firewall_client.ChatApi(api_client)
    request_body = None # Dict[str, object] | 

    try:
        # Firewall text chat endpoint
        api_response = api_instance.adapter_chat(request_body)
        print("The response of ChatApi->adapter_chat:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChatApi->adapter_chat: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request_body** | [**Dict[str, object]**](object.md)|  | 

### Return type

**Dict[str, object]**

### Authorization

Require authorization bearer token to be added in header.

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

