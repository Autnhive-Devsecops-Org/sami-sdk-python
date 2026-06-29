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
from sami_firewall_client.models.chat_message import ChatMessage
from sami_firewall_client.rest import ApiException
from pprint import pprint

# Configuration: host + bearer token (single source of truth)
HOST = "https://sami.autnhive.net"
BEARER_TOKEN = "sk_llm-XXXXXXXX-XXXXXXXX-XXXXXXXX-XXXXXXXX"  # dummy token, replace with your API key

configuration = sami_firewall_client.Configuration(host=HOST)
# Keep the token on the Configuration object as the single source of truth.
configuration.access_token = BEARER_TOKEN

# Build an ApiClient that applies the Authorization header on every request.
api_client = sami_firewall_client.ApiClient(
    configuration,
    header_name="Authorization",
    header_value=f"Bearer {configuration.access_token}",
)

# Enter a context with an instance of the API client
with api_client:
    # Create an instance of the API class
    api_instance = sami_firewall_client.ChatApi(api_client)
    chat_completion_request = ChatCompletionRequest(
        messages=[ChatMessage(role="user", content="capital of india")]
    ) # ChatCompletionRequest | 

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

