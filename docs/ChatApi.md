# sami_firewall_client.ChatApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**adapter_chat**](ChatApi.md#adapter_chat) | **POST** /ai-firewall/firewall/v1/prompt/text | Firewall text chat endpoint


# **adapter_chat**
> Dict[str, object] adapter_chat(chat_completion_request)

Firewall text chat endpoint

### Example

* Bearer Authentication (HTTPBearer):

```python
import sami_firewall_client
from sami_firewall_client.models.chat_completion_request import ChatCompletionRequest
from sami_firewall_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = sami_firewall_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: HTTPBearer
configuration = sami_firewall_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with sami_firewall_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sami_firewall_client.ChatApi(api_client)
    chat_completion_request = sami_firewall_client.ChatCompletionRequest() # ChatCompletionRequest | 

    try:
        # Firewall text chat endpoint
        api_response = api_instance.adapter_chat(chat_completion_request)
        print("The response of ChatApi->adapter_chat:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChatApi->adapter_chat: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **chat_completion_request** | [**ChatCompletionRequest**](ChatCompletionRequest.md)|  | 

### Return type

**Dict[str, object]**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

