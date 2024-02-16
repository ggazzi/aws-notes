- Each policy is an object/document that allows or denies access to AWS services.
  title:: AWS/IAM/Policy
- It doesn't determine which [identities]([[AWS/IAM/Identity]]) it applies to, a policy must be attached to them in [[AWS/IAM]].
- A variety of default policies are provided with every account:
	- AdministratorAccess: essentially, same permissions as the [[AWS/Root User]]