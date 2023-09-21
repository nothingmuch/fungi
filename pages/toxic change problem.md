- For illustrative purposes, assume 0 fees are possible
- This is a problem inherent in fixed denomination coinjoins even under this favorable assumption
- Scenario:
	- Alice has 2 coins, $A_1$ and $A_2$, worth $x$, the smallest denomination in use in a coinjoin implementation.
	- She coinjoins with using each separately, obtaining $A'_1$ and $A'_2$, each of which has $k$ identical siiblings
	- She makes two independent payments (avoiding temporal & network fingerprints), one producing chage outputs $A''_1$ and $A''_2$, such that $A''_1 + A''_2 >= x$. Note that each payment benefits from [[k-anonymity]] up to this point
		- assuming other parties in the mix do not undermine their own privacy, if the adversary can reliably detect this it is equivalent to a Sybil attack
	- Since $A''_1$ and $A''_2$ cannot be coinjoined separately, they must be combined, necessarily linking them together in the worst case, as the $k$-anonymity analysis no longer holds from this point