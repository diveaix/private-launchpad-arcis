# Private AMM v12 circuits (one SOL balance + per-token positions)

The trading-account circuits with a position input (SPEC §18): each order reads the account state (SOL) and its position state (token, sold) by reference and still outputs one state, so the callbacks are unchanged. `fast_sync_v2` also returns the merged state under the MXE. Source: branch `m4/trading-accounts` of the private launchpad prototype, `amm-v5/encrypted-ixs` (batches by `scripts/gen-acct.mjs`, lanes by `scripts/gen-lane.mjs`, `fast_sync_v2` by `scripts/gen-fast.mjs`). Arcium 0.15.0. Prototype only: unaudited, devnet test use.

| Circuit | Bytes | SHA-256 | Weight |
| --- | ---: | --- | --- |
| `acct_batch2_v7` | 6779836 | `0f579bbc8f6422cb72b5eda9c73a52545c8ebdaa981f2e9a4361e913ab478cbc` | 2.499e9 |
| `acct_batch4_v7` | 8193892 | `8e40471cab227ca74af2a5439a3471ee17f658da85944fc6dfb7eb561cbd071f` | 2.926e9 |
| `acct_batch8_v7` | 10970528 | `a242e5413713931a0dcbc208fa7e4c04fe54dccbfcf682b2c389759d3c251e09` | 3.778e9 |
| `acct_fund_v7` | 3862159 | `ab5208b64f09637ed17f72efcb4c9aa625641660d2ae263ef6c699659d7ec06e` | 1.295e9 |
| `acct_lane_b1_n2_s2_v7` | 13540304 | `900903352ffdfbc5563e9a470ab0bbc1c7405ac32560ed158e49a234808d0636` | 3.955e9 |
| `acct_lane_b1_n5_s1_v7` | 12350119 | `c9e16a49c6122ddb6c7609c534d676cb385e7f02d271f7103baead92d65c0b81` | 3.869e9 |
| `acct_lane_b2_n6_v7` | 14211740 | `05cbad00a5fcaf385a4a3ef9e44140b2b69d3d6f2746e91d77dca366a5a229a1` | 4.238e9 |
| `acct_lane_s2_v7` | 7080306 | `b042c3e67c13842d956c4bbfe4a29713da18f6aded0f45317cc17a03413d3def` | 2.427e9 |
| `acct_lane_s3_v7` | 10314406 | `3a3a2056c46f7269b1485bc7014d120060ae06d6ac0cbef8b4d62c89f6a66a91` | 3.155e9 |
| `acct_swap_v7` | 3782307 | `a91c63961ef1c23849d8eac2c7322c285917d362fdc87a31cdaaf7d2dbd2679e` | 1.686e9 |
| `acct_view_v7` | 304759 | `785b3f754b76934c9a84a5ae19b809f9dddb99360f57c40165876964da766cf0` | 0.221e9 |
| `acct_withdraw_v7` | 5950549 | `150357be4ed47afbd561dea69dff24aeb77d2dfe38d67d6753a7e2195806c0a3` | 1.297e9 |
| `fast_sync_v2` | 1273359 | `99c65672c76aa547e8421a1051ed588a50720d60d46ebd5cea27002591306f28` | 0.927e9 |
