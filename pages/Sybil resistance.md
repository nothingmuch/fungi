- A privacy enhancing system cannot actually enhance privacy if there is only one legitimate user
- However, without sybil resistance, this fully surveilled scenario is indistinguishable from the one where all users are legitimate
- It follows that the only way to resist Sybil based deanonymization attacks is to impose a cost on users
  - informally: sybil resistance is obtained by protocols for spending fees together with other users
- In particular, the transaction fees and the time value (so coindays destroyed) are unavoidable and can be used to estimate the cost that an active privacy [[adversary]] must incur in order to create the illusion of privacy for a specific user
- Note that for multiple users the math changes a bit
	- although targetting multiple users is harder than targeting one, it still gives the adversary an advantage
		- the cost of the setup can be shared
		- the marginal cost to deanonymize decreases expoentially with every successful attack
- if the costs to the adversary are prohibitive, then the privacy metrics can be seen as meaningful
	- prohibitive means:
		- total cost is larger than theft value of transaction(s)
		- and larger than TODO FIXME lower bound adjusted harm estimate
		- {{embed ((6505c008-06c3-4c6d-a639-123b75d7334a))}}
- imposing a cost
	- using a chain tip as a salt, the hash of an outpoint can be used to randomize "desireability" of a specific coin, all else being equal
	- if all clients agree on what is "desirable", this means they will make proposal to, and prefer coinjoining with, the same coins
	- similarly, pairs of inputs can have their XOR metric computed, with input sets being "close" to each other
		- these two values are analogous to proof of work, in that they are estimators of the number of coins that could have but did not participate in such a transaction, and that the coins that did participate were selected randomly (and verifiably so)
	- creating this structure is dramatically more costly to a single Sybil adversary, but costless for honest users with low time preference
		- also provides a symmetry breaking procedure, simplifying coalition formation
