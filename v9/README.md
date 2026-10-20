# Private AMM v9 circuits (M5 Fast mode)

Compiled Arcis circuits (Arcium 0.15.0) of the `private_amm_v5` program on branch `m4/trading-accounts` of the private launchpad prototype (commit 036c524, `amm-v5/encrypted-ixs`) added for M5 Fast mode (SPEC §16): the TEE's batches are re-run and checked by `fast_verify_v1`, and `fast_sync_v1` re-encrypts the pool, one trading account and its pad book to the TEE's x25519 key. Every other circuit stays under `v6/`, `v7/` and `v8/`. The devnet deployment pins each file by URL and SHA-256; Arcium nodes refuse a file whose hash differs.

Prototype only: unaudited, devnet test use.

| Circuit | Bytes | SHA-256 | Weight (depth) |
| --- | ---: | --- | --- |
| `fast_verify_v1` | 11820610 | `8665e981b681d7f6a192e430cba79c76396b77311d8d36551945c68b7af0c594` | 4.808e9 (750) |
| `fast_sync_v1` | 1221939 | `3502fa9033d7064afac4453dd068ca99e50206bd15c7a7db9b1710637bb1d3c2` | 0.887e9 (44) |
