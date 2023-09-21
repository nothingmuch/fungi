- interacting with bitcoin privately and securely requires:
	- generating secrets
	- ability to sign securely
		- secure [[secret storage]]
		- [[trusted computing base]] computing on secrets
		- broadcasting to the network might not require TCB in contrived circumstances, but generally does (e.g. to run a non backdoored version of tor)
	- blockchain information
		- wallet transactions
			- confirmed
			- unconfirmed
	- secure storage of auxiliarry information
		- txs & tx fragments
			- shared receive addresses
			- proposed but abandoned txs
				- payjoin precursors (e.g. BIP 78 replaced initial tx)
				- RBF replacements
				- unsigned txs
				- failed coinjoin session transcripts
		- user provided labeling information, constraints
		- known and trusted keys
			- update keys, server keys for coordination, ...
			- counterparties, cosigners, ...