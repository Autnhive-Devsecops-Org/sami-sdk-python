# IngestDocument


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**doc_id** | **str** | Optional document identifier | [optional] 
**text** | **str** | Document text/content | 
**metadata** | **Dict[str, object]** | Document metadata, including source_type | [optional] 

## Example

```python
from sami_rag_client.models.ingest_document import IngestDocument

# TODO update the JSON string below
json = "{}"
# create an instance of IngestDocument from a JSON string
ingest_document_instance = IngestDocument.from_json(json)
# print the JSON string representation of the object
print(IngestDocument.to_json())

# convert the object into a dict
ingest_document_dict = ingest_document_instance.to_dict()
# create an instance of IngestDocument from a dict
ingest_document_from_dict = IngestDocument.from_dict(ingest_document_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


