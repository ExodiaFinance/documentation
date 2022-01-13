# Stake Your EXOD (🧪,🧪)

Staking allows you to earn EXOD passively via auto-compounding. By staking your EXOD with EXODIA, you receive sEXOD (staked EXOD) in return at a 1:1 ratio. After that, your sEXOD balance will increase automatically on every epoch based on the current APY

## How to Buy EXOD

1. Go to [this SpookySwap swap page](https://spookyswap.finance/swap?inputCurrency=0x8D11eC38a3EB5E956B052f67Da8Bdc9bef8Abf3E\&outputCurrency=0x3b57f3feaaf1e8254ec680275ee6e7727c7413c7).
2. Make sure the output currency is EXOD. You can also copy and paste the EXOD contract address _0x3b57f3feaaf1e8254ec680275ee6e7727c7413c7_ into the output currency field to ensure you are swapping for the right token.
3. You can select any input currency based on your available wallet balance. It is recommended to use DAI as the input currency to minimize the slippage.
4. Select the amount of EXOD you want to swap for. Then click "Approve" and sign the transaction.
5. After the "Approve" transaction has been processed successfully, click "Swap" and sign the transaction.
6. You should see EXOD in your wallet balance now after the swap transaction is successful. If you cannot find it in your wallet, add EXOD contract address _0x3b57f3feaaf1e8254ec680275ee6e7727c7413c7_ to your wallet.

{% hint style="info" %}
The "Approve" transaction is only needed when you swap EXOD for the first time; subsequent swapping only requires you to perform the "Swap" transaction.
{% endhint %}

## How to Stake

1. Go to the [Stake page of the EXODIA website](https://app.exodia.fi/stake). Select the "Stake" tab.
2. Enter the amount of EXOD that you would like to stake in the input field. If you would like to stake all your EXOD, press the "Max" button and the input field will be populated with all your available EXOD balance.
3. Click "Approve" and sign the transaction.
4. After the "Approve" transaction has been processed successfully, click "Stake" and sign the transaction. Voila, you have staked your EXOD!

## How to Unstake

1. Go to the [Stake page of the EXODIA website](https://app.exodia.fi/stake). Select the "Unstake" tab.
2. Enter the amount of sEXOD that you would like to unstake in the input field. If you would like to unstake all your sEXOD press the "Max" button and the input field will be populated with all your available sEXOD balance.
3. Click "Approve" and sign the transaction.
4. After the "Approve" transaction has been processed successfully, click "Unstake" and sign the transaction.

_Note: The "Approve" transaction is only needed when staking/unstaking for the first time; subsequent staking/unstaking only requires you to perform the "Stake" or "Unstake" transaction._

## Reading the Info

**APY** tells you the annualized rate of return based on the reward yield. It takes into account the effect of compounding since sEXOD rebases exponentially.

**TVL** measures the dollar amount of all the staked EXOD in EXODIA.

**Current Index** allows you to track your gain from staking. The index started from 1 at epoch 0, and increases every epoch. If you staked at genesis (epoch 0) and never unstaked any EXOD, your balance today would be X times greater, where X is the current index. You can use the index to track your position by marking down the index number when you stake and unstake. You divide the index number when you unstake by the index number when you stake to get the ratio by which your sEXOD balance has increased.

**Your Balance** tells you how many unstaked EXOD are in your wallet. This is the maximum amount that you can stake.

**Your Staked Balance** tells you how many staked EXOD are in your wallet. This is the maximum amount that you can unstake.

**Next Rebase** tells you the remaining time until the next rebase.

**Reward Yield** tells you how much your sEXOD balance will increase when the next epoch begins. For example, if you stake 100 EXOD and the upcoming rebase is 0.5427%, your sEXOD balance would increase from 100 to 100.5427.

**ROI (5-Day Rate)** estimates how much your sEXOD balance will increase after 5 days, if the reward yield stays the same during this period. For example, if you stake 100 EXOD and the rate is 8.4577%, your sEXOD balance would increase from 100 to 108.4577 after 5 days.
