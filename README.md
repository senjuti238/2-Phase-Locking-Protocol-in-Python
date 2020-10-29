# 2-Phase-Locking-Protocol-in-Python
2-Phase Locking Protocol using Python 3

NAME:
two phase locking

How To Run
python demo.py

DESCRIPTION
Two-phase locking (2PL) is a concurrency control method that guarantees serializability. It is
also the name of the resulting set of database transaction schedules (histories). The protocol
utilizes locks, applied by a transaction to data, which may block other transactions from
accessing the same data during the transaction&#39;s life.
By the 2PL protocol, locks are applied and removed in two phases:
1.     Expanding phase: locks are acquired and no locks are released.
2.     Shrinking phase: locks are released and no locks are acquired.
Two types of locks are utilized by the basic protocol: Shared and Exclusive locks. Each line has a single transaction operation. The possible operations are: b (begin transaction), r (read item), w (write item), and e (end transaction). Each operation will be followed by a transaction id that is an integer between 1 and 99. For r and w operations, an item name follows between parentheses (item names are single letters from A to Z). An example is given below.

Example Input File:
IP1:

b1;
r1 (Y);
w1 (Y);
r1 (Z);
b2;
r2 (X);
w2 (X);
w1 (Z);
e1;
r2 (Y);
b3;
r3 (Z);
w3 (Z);       
w2 (Y);
e2;
r3 (X);
w3 (X);
e3;

Program first identifies what is the operation in method assignFunction and then it assigns different functions to begin transaction, readLock, writeLock, end transaction.

Output is printed to the console 
