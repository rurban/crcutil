Crcutil library provides efficient implementation of CRC algorithms. It includes reference implementation of a novel Multiword CRC algorithm invented by Andrew Kadatch and Bob Jenkins in early 2007. The new algorithm is heavily tuned towards modern Intel and AMD processors and is substantially faster than almost all other software CRC algorithms.

Included whitepaper describes the details of Multiword CRC algorithm as well as other algorithms and CRC manipulation routines implemented by crcutil library.

Crcutil library computes
  * Hardware-assisted CRC32C: 0.13 (Nehalem) CPU cycles per byte.
  * 64-bit and smaller CRCs: 1.0 (Nehalem) - 1.2 (Core) CPU cycles per byte.
  * 128-bit CRCs: 1.7 CPU cycles per byte.

Since computational speed of 64-bit CRCs is identical to 32-bit and 16-bit, the use of crcutil library enables widespread use of more reliable 64-bit CRCs instead of 32-bit ones.

As a bonus, crcutil also implements a number of useful CRC "tricks" (e.g. computation of CRC of concatenated blocks of data of known length and CRC without touching actual data).