# IngestCommitRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenant_id** | **str** |  | [optional] 
**app_id** | **str** |  | [optional] 
**store_quarantine** | **bool** |  | [optional] [default to True]
**retriever_backend** | **str** |  | [optional] 
**source_adapter** | **str** |  | [optional] 
**index** | **str** |  | [optional] 
**documents** | [**List[IngestDocument]**](IngestDocument.md) |  | 
**bucket** | **str** |  | [optional] 
**data_source_id** | **str** |  | [optional] 

## Example

```python
from sami_rag_client.models.ingest_commit_request import IngestCommitRequest

# TODO update the JSON string below
json = "{}"
# create an instance of IngestCommitRequest from a JSON string
ingest_commit_request_instance = IngestCommitRequest.from_json(json)
# print the JSON string representation of the object
print(IngestCommitRequest.to_json())

# convert the object into a dict
ingest_commit_request_dict = ingest_commit_request_instance.to_dict()
# create an instance of IngestCommitRequest from a dict
ingest_commit_request_from_dict = IngestCommitRequest.from_dict(ingest_commit_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


