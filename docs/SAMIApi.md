# sami_rag_client.SAMIApi

All URIs are relative to */rag-defender*

Method | HTTP request | Description
------------- | ------------- | -------------
[**approve_quarantine_doc**](SAMIApi.md#approve_quarantine_doc) | **POST** /v1/quarantine/{doc_id}/approve | Quarantine
[**ingest_commit**](SAMIApi.md#ingest_commit) | **POST** /v1/ingest | Data Ingestion
[**ingest_sync**](SAMIApi.md#ingest_sync) | **POST** /v1/ingest/sync | Ingest Sync
[**reject_quarantine_doc**](SAMIApi.md#reject_quarantine_doc) | **POST** /v1/quarantine/{doc_id}/reject | Reject Quarantine


# **approve_quarantine_doc**
> QuarantineReviewResponse approve_quarantine_doc(doc_id, quarantine_review_request, authorization=authorization)

Quarantine

Approve quarantined doc and move it to accepted status;
pushes to indexer when enabled.

### Example


```python
import sami_rag_client
from sami_rag_client.models.quarantine_review_request import QuarantineReviewRequest
from sami_rag_client.models.quarantine_review_response import QuarantineReviewResponse
from sami_rag_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /rag-defender
# See configuration.py for a list of all supported configuration parameters.
configuration = sami_rag_client.Configuration(
    host = "/rag-defender"
)


# Enter a context with an instance of the API client
with sami_rag_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sami_rag_client.SAMIApi(api_client)
    doc_id = 'doc_id_example' # str | Document ID
    quarantine_review_request = sami_rag_client.QuarantineReviewRequest() # QuarantineReviewRequest | 
    authorization = 'authorization_example' # str |  (optional)

    try:
        # Quarantine
        api_response = api_instance.approve_quarantine_doc(doc_id, quarantine_review_request, authorization=authorization)
        print("The response of SAMIApi->approve_quarantine_doc:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SAMIApi->approve_quarantine_doc: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **doc_id** | **str**| Document ID | 
 **quarantine_review_request** | [**QuarantineReviewRequest**](QuarantineReviewRequest.md)|  | 
 **authorization** | **str**|  | [optional] 

### Return type

[**QuarantineReviewResponse**](QuarantineReviewResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ingest_commit**
> IngestCommitResponse ingest_commit(authorization=authorization, ingest_commit_request=ingest_commit_request)

Data Ingestion

### Example


```python
import sami_rag_client
from sami_rag_client.models.ingest_commit_request import IngestCommitRequest
from sami_rag_client.models.ingest_commit_response import IngestCommitResponse
from sami_rag_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /rag-defender
# See configuration.py for a list of all supported configuration parameters.
configuration = sami_rag_client.Configuration(
    host = "/rag-defender"
)


# Enter a context with an instance of the API client
with sami_rag_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sami_rag_client.SAMIApi(api_client)
    authorization = 'authorization_example' # str |  (optional)
    ingest_commit_request = sami_rag_client.IngestCommitRequest() # IngestCommitRequest |  (optional)

    try:
        # Data Ingestion
        api_response = api_instance.ingest_commit(authorization=authorization, ingest_commit_request=ingest_commit_request)
        print("The response of SAMIApi->ingest_commit:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SAMIApi->ingest_commit: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **str**|  | [optional] 
 **ingest_commit_request** | [**IngestCommitRequest**](IngestCommitRequest.md)|  | [optional] 

### Return type

[**IngestCommitResponse**](IngestCommitResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ingest_sync**
> IngestSyncResponse ingest_sync(source=source, authorization=authorization, ingest_sync_request=ingest_sync_request)

Ingest Sync

### Example


```python
import sami_rag_client
from sami_rag_client.models.ingest_sync_request import IngestSyncRequest
from sami_rag_client.models.ingest_sync_response import IngestSyncResponse
from sami_rag_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /rag-defender
# See configuration.py for a list of all supported configuration parameters.
configuration = sami_rag_client.Configuration(
    host = "/rag-defender"
)


# Enter a context with an instance of the API client
with sami_rag_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sami_rag_client.SAMIApi(api_client)
    source = 'static_docs' # str |  (optional) (default to 'static_docs')
    authorization = 'authorization_example' # str |  (optional)
    ingest_sync_request = sami_rag_client.IngestSyncRequest() # IngestSyncRequest |  (optional)

    try:
        # Ingest Sync
        api_response = api_instance.ingest_sync(source=source, authorization=authorization, ingest_sync_request=ingest_sync_request)
        print("The response of SAMIApi->ingest_sync:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SAMIApi->ingest_sync: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **source** | **str**|  | [optional] [default to &#39;static_docs&#39;]
 **authorization** | **str**|  | [optional] 
 **ingest_sync_request** | [**IngestSyncRequest**](IngestSyncRequest.md)|  | [optional] 

### Return type

[**IngestSyncResponse**](IngestSyncResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reject_quarantine_doc**
> QuarantineReviewResponse reject_quarantine_doc(doc_id, quarantine_review_request, authorization=authorization)

Reject Quarantine

Reject quarantined doc and mark it as rejected.

### Example


```python
import sami_rag_client
from sami_rag_client.models.quarantine_review_request import QuarantineReviewRequest
from sami_rag_client.models.quarantine_review_response import QuarantineReviewResponse
from sami_rag_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /rag-defender
# See configuration.py for a list of all supported configuration parameters.
configuration = sami_rag_client.Configuration(
    host = "/rag-defender"
)


# Enter a context with an instance of the API client
with sami_rag_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sami_rag_client.SAMIApi(api_client)
    doc_id = 'doc_id_example' # str | Document ID
    quarantine_review_request = sami_rag_client.QuarantineReviewRequest() # QuarantineReviewRequest | 
    authorization = 'authorization_example' # str |  (optional)

    try:
        # Reject Quarantine
        api_response = api_instance.reject_quarantine_doc(doc_id, quarantine_review_request, authorization=authorization)
        print("The response of SAMIApi->reject_quarantine_doc:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SAMIApi->reject_quarantine_doc: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **doc_id** | **str**| Document ID | 
 **quarantine_review_request** | [**QuarantineReviewRequest**](QuarantineReviewRequest.md)|  | 
 **authorization** | **str**|  | [optional] 

### Return type

[**QuarantineReviewResponse**](QuarantineReviewResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

