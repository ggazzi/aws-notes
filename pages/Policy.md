alias:: Policies

- Each policy is an object/document that allows or denies access to AWS services.
- It doesn't determine which [[Identities]] it applies to, a policy must be attached to them in [[IAM]].
- A variety of default policies are provided with every account:
	- AdministratorAccess: essentially, same permissions as the [[Root User]]