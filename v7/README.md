# Private AMM v7 circuits (M4 right-sized batches and lanes)

Compiled Arcis circuits (Arcium 0.15.0) of the `private_amm_v5` program on branch `m4/trading-accounts` of the private launchpad prototype (commit 96a8514, `amm-v5/encrypted-ixs`) that are new since `v6/`: the right-sized account batches (`acct_batch{2,4,8}_v5`, SPEC §15.7) and the lane circuits (several pools in one computation, SPEC §15.8). Every other circuit the program references is unchanged and stays pinned under `v6/` (same bytes). The devnet deployment pins each file by URL and SHA-256; Arcium nodes refuse a file whose hash differs.

Prototype only: unaudited, devnet test use.

| Circuit | Bytes | SHA-256 |
| --- | ---: | --- |
| `acct_batch2_v5` | 7026510 | `9b5ac419d5c987ce6601ba2d2f68d1ef9687f156ef9f19d76770cd23c29fd05a` |
| `acct_batch4_v5` | 8651538 | `413e1019934c24457ffd3b5314ef7ff25bca9ddb0489333d9840d7700c8e06b7` |
| `acct_batch8_v5` | 11850074 | `54f5059e4416c049cb9f9581c977efafabb016e51f07e9fc977028bf77a113fd` |
| `acct_lane_b1_n2_s2_v5` | 13746368 | `129a9b259c27ecccc46ec2534a2e997592aa4986acfe148bea58e7c954de85be` |
| `acct_lane_b1_n5_s1_v5` | 12896975 | `8d68ff8e7d947cdcead0dd61af904382fe8f7817e7b7c42acf52138203d43628` |
| `acct_lane_b2_n6_v5` | 14848683 | `6db685fd78def3eb93d05994bcb51a5a38bc7f4f86e5ded239aa08bc5104aba4` |
| `acct_lane_s2_v5` | 7030054 | `41ac745821e0e350c24ee065bd3f7f355073767c526af1921a7abae3cc42657c` |
| `acct_lane_s3_v5` | 10239110 | `5990b9eb5b5fcb3388b843812b78c551317a24e2a1283f3b91f4cca7237889e3` |
