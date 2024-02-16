alias:: CIDR

- See [Wikipedia article](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)
- Standard for allocating IP addresses for IP routing
	- Describes how to split addresses into a network prefix and host identifier, for variable-length network prefixes
	- No longer relies on the 3 most significant bits to determine length of network prefixes, as the previous "classful" architecture of IPv4 did
	- Also has a whole standard on how to allocate IP addresses and subnets
- Provides a notation for IP addresses and network masks:
	- Appends `/` and a decimal number to the traditional IPv4 or IPv6 address
	- The decimal number is the length of the network prefix (so indicates the number of 1-bits in the network mask)
	- Can be used to represent specific addresses, or an entire (sub)network
		- When the host identifier is 0, represent the network, example: 192.168.1.0/24
		- Otherwise, represents a specific host, example: 192.168.0.1