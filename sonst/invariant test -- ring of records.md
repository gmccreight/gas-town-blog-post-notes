^ [[invariant test]] -- ring of records

---

The tests creates a cycle (basically a ring of records) in the database where records point to each other in a cycle of a specific length.
:
Then the test system does thousands of transactions per second, moving the data around in transactions.  Each transaction makes changes that keep the cycle complete and the same length. At the end of the test it checks whether the cycle is still a cycle, and that it's still the same length.