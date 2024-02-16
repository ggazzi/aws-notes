- An AWS account is a container for [identities]([[AWS/IAM/Identity]]) and [[Resources]].
  title:: AWS/Account
- Every account has a [[AWS/Root User]].
- Associated to an e-mail address and payment method.
	- Usage of any resources in this account will be billed to this payment method.
- By default, nothing outside an account can do anything with the account's resources.
	- External identities can be granted access (including other AWS accounts), but this must be done explicitly.
- Separating an application into multiple accounts can contain the impact of [[Security]] breaches or admin errors.