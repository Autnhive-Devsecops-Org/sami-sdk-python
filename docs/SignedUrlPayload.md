# SignedUrlPayload

Request body for signed URL batch processing.  Attributes:     jobs            (List[Job]):      List of signed URL jobs.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**jobs** | [**List[Job]**](Job.md) |  | 

## Example

```python
from sami_firewall_client.models.signed_url_payload import SignedUrlPayload

# TODO update the JSON string below
json = "{}"
# create an instance of SignedUrlPayload from a JSON string
signed_url_payload_instance = SignedUrlPayload.from_json(json)
# print the JSON string representation of the object
print(SignedUrlPayload.to_json())

# convert the object into a dict
signed_url_payload_dict = signed_url_payload_instance.to_dict()
# create an instance of SignedUrlPayload from a dict
signed_url_payload_from_dict = SignedUrlPayload.from_dict(signed_url_payload_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


