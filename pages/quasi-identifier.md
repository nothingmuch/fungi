- attributes of a a user which on their own are not unique, but do contain some identifying information
- combinations of quasi identifiers can effectively a [[unique identifier]], see [[k-anonymity]]
- examples
	- date of birth
	- ip address
	- temporal observations
	- transaction fingerprints
		- properties of the transaction itself
		- properties of related transactions on the transaction graph
	- attributes which can only be attributed to the entity by virtue of the system it is using to interact, e.g. the chosen rendezvous node of a tor circuit might for example indicate something about the client's internal state
- non examples
	- ephemeral payloads indistinguishable from noise