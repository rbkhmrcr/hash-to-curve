# Hashing to Elliptic Curves

**IETF Data Tracker**: [draft-irtf-cfrg-hash-to-curve](https://datatracker.ietf.org/doc/draft-irtf-cfrg-hash-to-curve)

**Internet-Draft**: [git repository](https://github.com/cfrg/draft-irtf-cfrg-hash-to-curve)

This document specifies a number of algorithms that may be used to encode or hash an arbitrary string to a point on an elliptic curve.

### Warning

This implementation is **not** protected against any kind of attack,
including side-channel attacks. It **MUST NOT** be used in production systems.

Only the indifferentiable hashes to elliptic curves have been implemented and 
exposed here, to avoid misuse of non-uniform hash functions.

### License

BSD 3-Clause License

## Suites 
### NIST P-256
P256_XMD:SHA-256_SSWU_RO_ is defined as follows:
- encoding type: hash_to_curve
- E: y^2 = x^3 + A * x + B, where:
    - A = -3
    - B = 0x5ac635d8aa3a93e7b3ebbd55769886bc651d06b0cc53b0f63bce3c3e27d2604b
- p: 2^256 - 2^224 + 2^192 + 2^96 - 1
- m: 1
- k: 128
- expand_message: expand_message_xmd
- Hash: SHA-256
- L: 48
- f: Simplified SWU method
- Z: -10
- h_eff: 1
### NIST P-384
P384_XMD:SHA-384_SSWU_RO_ is defined as follows:
- encoding type: hash_to_curve
- E: y^2 = x^3 + A * x + B, where:
    - A = -3
    - B = 0xb3312fa7e23ee7e4988e056be3f82d19181d9c6efe8141120314088f5013875ac656398d8a2ed19d2a85c8edd3ec2aef
- p: 2^384 - 2^128 - 2^96 + 2^32 - 1
- m: 1
- k: 192
- expand_message: expand_message_xmd
- H: SHA-384
- L: 72
- f: Simplified SWU method
- Z: -12
- h_eff: 1

