# Private AMM v8 circuits (M5 hot tokens: trimmed batch rule work)

Compiled Arcis circuits (Arcium 0.15.0) of the `private_amm_v5` program on branch `m4/trading-accounts` of the private launchpad prototype (commit f57bbaf, `amm-v5/encrypted-ixs`) that changed since `v7/`: the account batches and the lane shapes with batch sections, whose per-order rule work was trimmed without changing any result (SPEC §15.9: the fee computed once, a u64 hourly-cap test, size-bucket thresholds from the public supply). They carry new names (`_v6`) because a comp def is addressed by its circuit name. `acct_lane_s2_v5` / `acct_lane_s3_v5` are unchanged and stay under `v7/`; every other circuit stays under `v6/`. The devnet deployment pins each file by URL and SHA-256; Arcium nodes refuse a file whose hash differs.

Prototype only: unaudited, devnet test use.

| Circuit | Bytes | SHA-256 | Weight (depth); before |
| --- | ---: | --- | --- |
| `acct_batch2_v6` | 6727896 | `ba1b58558d8f0fc5b6c6eda112d9dd9e8ebc7493158fa89ce58db5856946566e` | 2.457e9 (536); 2.557e9 (561) |
| `acct_batch4_v6` | 8100852 | `9f22539fd8ac6bf8c8c4bd0d0accd7cd543f5ffdcf966b780cf85a275a8fbdcd` | 2.842e9 (537); 2.989e9 (562) |
| `acct_batch8_v6` | 10786360 | `60b9baa47b10bb67e9e2861cd92c77a41e1a35a87b19de34975649cf10216790` | 3.609e9 (538); 3.849e9 (563) |
| `acct_lane_b1_n5_s1_v6` | 12208851 | `e2228d49f7de241c3fc8e9a3ed0505107076d8364a7f145e1fff05830f3fb8a0` | 3.742e9 (538); 3.912e9 (563) |
| `acct_lane_b1_n2_s2_v6` | 13438384 | `0460eee6daf3b0e421aeb0b4f86de655f388aaef1c246621ff2a37accd31a3a7` | 3.871e9 (537); 3.971e9 (562) |
| `acct_lane_b2_n6_v6` | 14072204 | `05c65d5450f4be46f40acf08fccd4fd0fa22d659e76ca0c4aedfccda6fc01b31` | 4.112e9 (538); 4.305e9 (563) |
