alias:: ARN

- An ARN uniquely references a resource within AWS.
- You can use wildcards to reference multiple resources.
- Follows specific [formats](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference-arns.html)
	- arn:_partition_:_service_:_region_:_account-id_:_resource-id_
	- arn:_partition_:_service_:_region_:_account-id_:_resource-type_/_resource-id_
	- arn:_partition_:_service_:_region_:_account-id_:_resource-type_:_resource-id_
- See [[AWS/Partition]], [[AWS/Region]], [[AWS/Account]]
- Fields may be omitted if they're not relevant
	- Example: [S3 buckets]([[S3 Bucket]]) don't have a _region_ or _account-id_, as the _resource-id_ is already unique across all of them