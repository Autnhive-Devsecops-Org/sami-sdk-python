# sami_firewall_client.DefaultApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**file_sanitization**](DefaultApi.md#file_sanitization) | **POST** /ai-firewall/firewall/v1/file/sanitization | Replace content in uploaded files
[**multimodal_chat**](DefaultApi.md#multimodal_chat) | **POST** /ai-firewall/firewall/v1/prompt | Multimodal chat completions


# **file_sanitization**
> List[str] file_sanitization(signed_url_payload)

Replace content in uploaded files

### Example

* Bearer Authentication (HTTPBearer):

```python
import sami_firewall_client
from sami_firewall_client.models.signed_url_payload import SignedUrlPayload
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
    api_instance = sami_firewall_client.DefaultApi(api_client)
    signed_url_payload = sami_firewall_client.SignedUrlPayload() # SignedUrlPayload | 

    try:
        # Replace content in uploaded files
        api_response = api_instance.file_sanitization(signed_url_payload)
        print("The response of DefaultApi->file_sanitization:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->file_sanitization: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **signed_url_payload** | [**SignedUrlPayload**](SignedUrlPayload.md)|  | 

### Return type

**List[str]**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | file replacement results |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **multimodal_chat**
> Dict[str, object] multimodal_chat(prompt=prompt, content=content, text=text, input=input, file=file, docx=docx, pdf=pdf, image=image, audio=audio, model=model)

Multimodal chat completions

### Example

* Bearer Authentication (HTTPBearer):

```python
import sami_firewall_client
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
    api_instance = sami_firewall_client.DefaultApi(api_client)
    prompt = 'prompt_example' # str | Free-form prompt text (optional)
    content = 'content_example' # str | Optional content payload (optional)
    text = 'text_example' # str | Optional text input (optional)
    input = 'input_example' # str | Optional input input (optional)
    file = None # bytes | Generic file upload (optional) (optional)
    docx = None # bytes | DOCX upload (optional) (optional)
    pdf = None # bytes | PDF upload (optional) (optional)
    image = None # bytes | Image upload (optional) (optional)
    audio = None # bytes | Audio upload (optional) (optional)
    model = 'model_example' # str | Optional model name (optional)

    try:
        # Multimodal chat completions
        api_response = api_instance.multimodal_chat(prompt=prompt, content=content, text=text, input=input, file=file, docx=docx, pdf=pdf, image=image, audio=audio, model=model)
        print("The response of DefaultApi->multimodal_chat:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->multimodal_chat: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **prompt** | **str**| Free-form prompt text | [optional] 
 **content** | **str**| Optional content payload | [optional] 
 **text** | **str**| Optional text input | [optional] 
 **input** | **str**| Optional input input | [optional] 
 **file** | **bytes**| Generic file upload (optional) | [optional] 
 **docx** | **bytes**| DOCX upload (optional) | [optional] 
 **pdf** | **bytes**| PDF upload (optional) | [optional] 
 **image** | **bytes**| Image upload (optional) | [optional] 
 **audio** | **bytes**| Audio upload (optional) | [optional] 
 **model** | **str**| Optional model name | [optional] 

### Return type

**Dict[str, object]**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | AI firewall chat completion response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

