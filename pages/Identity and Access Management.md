alias:: IAM

- Each [[AWS Account]] has a single instance of IAM, and this instance is fully trusted by the account.
- Three main responsibilities:
	- ID Provider
		- Management of [[Identities]] and [[Policies]], including which policies are attached to which identities.
	- Authentication
		- Ensuring that identities are who they claim to be
		- Various methods and [[Credentials]]
			- Passwords
			- MFA
			- [[Access Keys]] for CLI or API access
		- Provides a customisable sign-in URL for [[Users]]
	- Authorisation
		- Allowing or denying access to resources, whenever an identity tries to do something on the account.
- No cost, but there are limits to the number of identities and policies it has
- Global service
- No direct control on external accounts or users
	- Supports [[Identity Federation]]
- Minimising the permissions of each identity limits the impact of [[Security]] breaches.