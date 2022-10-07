# How to manually redeem using Avalanche's Snowtrace Explorer:

1. You need AVAX in your wallet in order to interact with the redemption contract. You can purchase AVAX on most CEX:es, you can also bridge tokens from Harmony to Avalanche using Synapse and get a small amount of AVAX to cover gas fees.

2. To interact with the contract you usually only need a couple of cents worth of AVAX, but we recommend funding your wallet with at least 0.03 - 0.05 AVAX to perform the redemption and then having sufficient AVAX for gas to send the native USDC to a CEX or performing additional onchain activities.

3. Open the [claims.json](claims.json) file and search for your wallet address.

4. Pay attention to the `"amountIn"`, `"account"`, `"amount"`, and `"merkleProof"` variables and their respective values next your address / within the same surrounding `{}` block. You will need these values for the next steps.

5. [Open the redemption contract on Snowtrace](https://snowtrace.io/address/0x0c4ce0a639a0e88c380520aa4a8e5a31c3921364#writeContract) in a separate tab or window.

6. Click on `"Connect to Web3"` and connect MetaMask to Snowtrace. 

7. Click on `"2. exchangeForAssets"`

8. Now enter the values for the `"amountIn"`, `"account"`, `"amount"`, and `"merkleProof"` variables that matches your wallet in [claims.json](claims.json). **IMPORTANT: Enter the values without quotes.**

9. For the `"merkleProof"` field you need to combine the entire array/list into a single long string where every array/list member is separated by a comma. **IMPORTANT: Enter the values without quotes.**

10. Click on `"Write"` and sign the transaction using MetaMask.

11. If the redemption was successful you should now have received native USDC in your wallet on Avalanche. You can add native USDC to your MetaMask by going to [Trader JOE](https://traderjoexyz.com/trade), selecting `"USDC"` as the `"To"` token, then clicking on the `"Add USDC to Wallet"` link below the `"Enter an amount"` button. You can also add it directly in MetaMask as a custom token using the contract address `0xB97EF9Ef8734C71904D8002F8b6Bc66Dd9c48a6E`.

12. USDC is not the same as USDC.e which is the bridged version of USDC from Ethereum. Avalanche's native version of USDC is unfortunately not widely available on all CEX:es and you will have to pay attention to this when depositing. Otherwise you can end up losing your funds if you deposit to a CEX that does not support native Avalanche USDC.

13. Binance (non US), Huobi, and OKX are some CEX:es that support native Avalanche USDC.

14. If you do not have access to these CEX:es you can swap your native USDC for bridged USDC.e using e.g. [GMX](https://app.gmx.io/#/trade) or [TraderJoe](https://traderjoexyz.com/trade).

15. Your USDC.e can then be deposited to CEX:es that support USDC.e (e.g. Crypto.com) or be bridged back to Ethereum using [Avalanche's bridge](https://bridge.avax.network/). USDC bridged back to Ethereum can then be deposited to any CEX that supports Ethereum ERC-20 USDC.

16. You can also convert all of your USDC to AVAX and then deposit that to CEX:es (make sure the CEX:es support Avalanche C-Chain deposits).
