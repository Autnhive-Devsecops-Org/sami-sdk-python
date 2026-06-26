# Job

Represents a single signed URL processing job.  Attributes:     id: str                    Tracking ID for the job — used for logging and tracing.     signed_url (str):          Pre-signed URL to download input file.     file_name  (str):          File name with extension — used to detect                                file type when URL has no extension.     file_size  (Optional[int]):File size in bytes — used for logging only.     enhanced_privacy_mode (bool): Flag to indicate if enhanced privacy mode is enabled for this job.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**signed_url** | **str** |  | 
**file_name** | **str** |  | 
**policy_packs** | **List[str]** |  | 
**file_size** | **int** |  | [optional] 
**enhanced_privacy_mode** | **bool** |  | [optional] [default to False]

## Example

```python
from sami_firewall_client.models.job import Job

# TODO update the JSON string below
json = "{}"
# create an instance of Job from a JSON string
job_instance = Job.from_json(json)
# print the JSON string representation of the object
print(Job.to_json())

# convert the object into a dict
job_dict = job_instance.to_dict()
# create an instance of Job from a dict
job_from_dict = Job.from_dict(job_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


