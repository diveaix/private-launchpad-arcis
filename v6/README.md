# Private AMM v6 circuits (M4-B trading accounts)

Compiled Arcis circuits (Arcium 0.15.0) of the `private_amm_v5` program on branch `m4/trading-accounts` of the private launchpad prototype (commit 7bdef5c, `amm-v5/encrypted-ixs`): the M2–M4.1 circuits rebuilt since `v5/` plus the M4-B trading-account circuits. The devnet deployment pins each file by URL and SHA-256; Arcium nodes refuse a file whose hash differs.

Prototype only: unaudited, devnet test use.

| Circuit | Bytes | SHA-256 |
| --- | ---: | --- |
| `acct_batch_v5` | 10944151 | `05294e36ea47c5078906ab33110ba3b15cd84d9a7259d7473dab84e0031fddc0` |
| `acct_fund_v5` | 3835407 | `9f3ae1796bfc76003ab22bb777773bd23e13d10032d6484b7fc972634a4e6c9a` |
| `acct_refill_v5` | 931251 | `b5354a0b58a8d87ba8c8d8328cdad1a9e5a88f451e9cecaa8ebaa3a9b6658e51` |
| `acct_swap_v5` | 3754611 | `e27c437e768c7f1db9c9e494e5affb9c3453c04bbab1a65c3045e3014fa4c2e8` |
| `acct_view_v5` | 219603 | `6abb2ee8663b2faa3458fb227b856c75cd5ca0fe96258b7b2e8b48fad73a18ba` |
| `acct_withdraw_v5` | 5916866 | `287fdb103577b94e8744367b45c8177a6f2e382daa8c5f9c66de4f071de88bb8` |
| `auction_clear_v5` | 7182164 | `50785feaf01677500ef8825660bbf7c57d3d182f6f930e5518019eebef925344` |
| `auction_commit_v5` | 3029707 | `63bdeedb76e885da5e64fd107750829fcc1008b4c64dfbe466489f25582df9df` |
| `auction_payout_v5` | 3197214 | `a25be54cbb9c92845a260b944cea8968de4a814f92d3e99a33fc47942a4f2879` |
| `auction_sum_v5` | 2194111 | `cf570d17701bc7a69a635bb7e9ace62039153b1e692eac0d2fe30e1358210f8f` |
| `batch_commit_v5` | 3112930 | `cb13acbb447ce3b724c150226f7cd69ccad7e5b46d6ce65bd97f95d7e58f6b0b` |
| `batch_fill_v5` | 6812061 | `7e91433228b218db7c557730450b890d66ed1ad300b9edca03b6602feab0e40c` |
| `batch_payout_v5` | 3741898 | `b05cfa9678990fc55d0fd6872c89190cae3c63207a39c4af20e999b4e2dbcd14` |
| `batch_price_v5` | 3390822 | `ec6202654c8be188fe1bbf32c5ba96cb0594c1cede12442c49e6ac1a6079d96d` |
| `claim_fees_v5` | 3168331 | `f984b7c7b7a9b82f768450605f0d3fc914676484467c2d601d52b9649604bf52` |
| `feed_refill_v5` | 931251 | `b5354a0b58a8d87ba8c8d8328cdad1a9e5a88f451e9cecaa8ebaa3a9b6658e51` |
| `init_pool_v5` | 63251 | `25afc33ca9b78aa0130abd0ec6d7f36692f83d9157d1e244260a43df14e69709` |
| `snapshot_v5` | 347631 | `af2a05ccc744a43248e291a1d4e60beb753639c0971d6267b8e2f187f7e39a58` |
| `swap_v5` | 9499707 | `b5082b726e5a4482b3c5d46b5992dc6248a980ca8fe3475f0849e68426b6ef1c` |

`acct_refill_v5` and `feed_refill_v5` compile to identical bytes (same body, two computation definitions).
