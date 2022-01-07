# FAQ

## Why do we need EXODIA in the first place?

Dollar-pegged stablecoins have become an essential part of crypto due to their lack of volatility as compared to tokens such as Bitcoin and Ether. Users are comfortable with transacting using stablecoins knowing that they hold the same amount of purchasing power today vs. tomorrow. But this is a fallacy. The dollar is controlled by the US government and the Federal Reserve. This means a depreciation of dollar also means a depreciation of these stablecoins.

EXODIA aims to solve this by creating a free-floating reserve currency, EXOD, that is backed by a basket of assets. By focusing on supply growth rather than price appreciation, EXODIA hopes that EXOD can function as a currency that is able to hold its purchasing power regardless of market volatility.

## Is EXOD a stablecoin?

No, EXOD is not a stablecoin. Rather, EXOD aspires to become an algorithmic reserve currency backed by other decentralized assets. Similar to the idea of the gold standard, EXOD provides free floating value its users can always fall back on, simply because of the fractional treasury reserves EXOD draws its intrinsic value from.

## EXOD is backed, not pegged.

Each EXOD is backed by 1 DAI, not pegged to it. Because the treasury backs every EXOD with at least 1 DAI, the protocol would buy back and burn EXOD when it trades below 1 DAI. This has the effect of pushing EXOD price back up to 1 DAI. EXOD could always trade above 1 DAI because there is no upper limit imposed by the protocol. Think pegged == 1, while backed >= 1.

You might say that the EXOD floor price or intrinsic value is 1 DAI. We believe that the actual price will always be 1 DAI + premium, but in the end that is up to the market to decide.

## How does it work?

At a high level, EXODIA consists of its protocol managed treasury, protocol owned liquidity (POL), bond mechanism, and staking rewards that are designed to control supply expansion.

Bond sales generate profit for the protocol, and the treasury uses the profit to mint EXOD and distribute them to stakers. With liquidity bonds, the protocol is able to accumulate its own liquidity.

## What is the deal with (3,3) and (1,1)?

(3,3) is the idea that, if everyone cooperated in EXODIA, it would generate the greatest gain for everyone (from a [game theory](https://en.wikipedia.org/wiki/Game\_theory) standpoint). Currently, there are three actions a user can take:

* Staking (+2)
* Bonding (+1)
* Selling (-2)

Staking and bonding are considered beneficial to the protocol, while selling is considered detrimental. Staking and selling will also cause a price move, while bonding does not (we consider buying EXOD from the market as a prerequisite of staking, thus causing a price move). If both actions are beneficial, the actor who moves price also gets half of the benefit (+1). If both actions are contradictory, the bad actor who moves price gets half of the benefit (+1), while the good actor who moves price gets half of the downside (-1). If both actions are detrimental, which implies both actors are selling, they both get half of the downside (-1).

Thus, given two actors, all scenarios of what they could do and the effect on the protocol are shown here:

![](../.gitbook/assets/game\_theory.png)

* If we both stake (3, 3), it is the best thing for both of us and the protocol (3 + 3 = 6).
* If one of us stakes and the other one bonds, it is also great because staking takes EXOD off the market and put it into the protocol, while bonding provides liquidity and DAI for the treasury (3 + 1 = 4).
* When one of us sells, it diminishes effort of the other one who stakes or bonds (1 - 1 = 0).
* When we both sell, it creates the worst outcome for both of us and the protocol (-3 - 3 = -6).

## Why is PCV important?

As the protocol controls the funds in its treasury, EXOD can only be minted or burned by the protocol. This also guarantees that the protocol can always back 1 EXOD with 1 DAI. You can easily define the risk of your investment because you can be confident that the protocol will indefinitely buy EXOD below 1 DAI with the treasury assets until no one is left to sell. You can't trust the FED but you can trust the code.

As the protocol accumulates more PCV, more runway is guaranteed for the stakers. This means the stakers can be confident that the current staking APY can be sustained for a longer term because more funds are available in the treasury.

## Why is POL important?

EXODIA owns most of its liquidity thanks to its bond mechanism. This has several benefits:

* EXODIA does not have to pay out high farming rewards to incentivize liquidity providers a.k.a renting liquidity.
* EXODIA guarantees the market that the liquidity is always there to facilitate sell or buy transaction.
* By being the largest LP (liquidity provider), it earns most of the LP fees which represents another source of income to the treasury.
* All POL can be used to back EXOD. The LP tokens are marked down to their risk-free value for this purpose.&#x20;

## Why is the market price of EXOD so volatile?

It is extremely important to understand how early in development the EXODIA protocol is. A large amount of discussion has centered around the current price and expected a stable value moving forward. The reality is that these characteristics are not yet determined. The network is currently tuned for expansion of EXOD supply, which when paired with the staking, bonding, and yield mechanics of EXODIA, result in a fair amount of volatility.

EXOD could trade at a very high price because the market is ready to pay a hefty premium to capture a percentage of the current market capitalization. However, the price of EXOD could also drop to a large degree if the market sentiment turns bearish. We would expect significant price volatility during our growth phase so please **do your own research** whether this project suits your goals.

## What is the point of buying it now when EXOD trades at a very high premium?

When you buy and stake EXOD, you capture a percentage of the supply (market cap) which will remain close to a constant. This is because your staked EXOD balance also increases along with the circulating supply. The implication is that if you buy EXOD when the market cap is low, you would be capturing a larger percentage of the market cap.

## What is a rebase?

Rebase is a mechanism by which your staked EXOD balance increases automatically. When new EXOD are minted by the protocol, a large portion of it goes to the stakers. Because stakers only see staked EXOD balance instead of EXOD, the protocol utilizes the rebase mechanism to increase the staked EXOD balance so that 1 staked EXOD is always redeemable for 1 EXOD.

## What is reward yield?

Reward yield is the percentage by which your staked EXOD balance increases on the next epoch. It is also known as _rebase rate_. You can find this number on the [EXODIA staking page](https://app.exodia.finance/#/stake).

## What is APY?

APY stands for annual percentage yield. It measures the real rate of return on your principal by taking into account the effect of compounding interest. In the case of EXODIA, your staked EXOD represents your principal, and the compound interest is added periodically on every epoch (28800 Fantom blocks, or around 8 hours) thanks to the rebase mechanism.

One interesting fact about APY is that your balance will grow not linearly but exponentially over time! Assuming a daily compound interest of 2%, if you start with a balance of 1 EXOD on day 1, after a year, your balance will grow to about 1377. That is a lot!

## How is the APY calculated?

The APY is calculated from the reward yield (a.k.a rebase rate) using the following equation:

$$
APY = ( 1 + rewardYield )^{1095}
$$

It raises to the power of 1095 because a rebase happens 3 times daily. Consider there are 365 days in a year, this would give a rebase frequency of 365 \* 3 = 1095.

Reward yield is determined by the following equation:

$$
rewardYield = EXOD_{distributed} / EXOD_{totalStaked}
$$

The number of EXOD distributed to the staking contract is calculated from EXOD total supply using the following equation:

$$
EXOD_{distributed} = EXOD_{totalSupply} \times rewardRate
$$

## Why does the price of EXOD become irrelevant in long term?

As illustrated above, your EXOD balance will grow exponentially over time thanks to the power of compounding. Let's say you buy an EXOD for $400 now and the market decides that in 1 year time, the intrinsic value of EXOD will be $2. Assuming a daily compound interest rate of 2%, your balance would grow to about 1377 EXODs by the end of the year, which is worth around $2754. That is a cool $2354 profit! By now, you should understand that you are paying a premium for EXOD now in exchange for a long-term benefit. Thus, you should have a long time horizon to allow your EXOD balance to grow exponentially and make this a worthwhile investment.

## What will be EXOD's intrinsic value in the future?

There is no clear answer for this, but the intrinsic value can be determined by the treasury performance. For example, if the treasury could guarantee to back every EXOD with 100 DAI, the intrinsic value will be 100 DAI.

## How does the protocol manage to maintain the high staking APY?

Let’s say the protocol targets an APY of 100,000%. This would translate to a rebase rate of about 0.6328%, or a daily growth of about 2%. Please refer to the equation above to learn how APY is calculated from the rebase rate.

If there are 100,000 of EXOD staked right now, the protocol would need to mint an additional 2000 EXOD to achieve this daily growth. This is achievable if the protocol can bring in at least 2000 DAI daily from bond sales. If the protocol fails to achieve this, the APY of 100,000% cannot be guaranteed.

## Do I have to unstake and stake EXOD on every epoch to get my rebase rewards?

No. Once you have staked EXOD with EXODIA, your staked EXOD balance will auto-compound on every epoch. That increase in balance represents your rebase rewards.

## What will happen if there is a bank run on Exodia?

We're using OHM as an example, as Dune analytics is not available for Fantom.

Fractional reserve banking works because depositors don’t withdraw their funds all at once. A depositor’s faith in the banking system rests on regulations and agencies like Federal Deposit Insurance Corporation (FDIC).

OHM does not have FDIC insurance but it has an incentive structure that protects stakers. Let’s take a look at how it performs during a hypothetical bank run. In this scenario, we assume the majority of stakers would panic and unstake their tokens from Olympus - the staking percentage which stands at 92% now quickly collapses to 3.3%, leaving only 55,000 OHM staked.

Next, we assume the Risk-Free Value (RFV) inflows to the treasury completely dry up. For context, RFV is currently growing at about 1$ million every 2 days ([source from Olympus queries](https://dune.xyz/queries/29153/58862)). However, during a bank run this growth will likely stop.

Finally, we assume that those last standing stakers bought in at a price of $500 per OHM. The initial investment of these stakers would be:

$$
$500/OHM*55000OHM=$27.5 millions
$$

As of September 15 2021, the total OHM supply is 2,082,553 and the RFV is $47,041,833. Remember that 1 OHM is backed by 1 USD (DAI or FRAX). By subtracting these two numbers, we know 44,959,280 OHM will eventually get issued to the remaining stakers. In roughly a year, these stakers who are holding 55,000 OHM will have:

$$
55000+44959280 = 45014280
$$

$27.5 million investment made by these stakers will turn into about $45 million based on cash flow alone if they stay staked (recall that 1 OHM is backed by 1 USD). In this bank run scenario, the stakers who stay staked not only get their money back, but also make some profit. Therefore, [(3,3)](faq.md#what-is-the-deal-with-3-3-and-1-1) isn’t just a popular meme, it is actually a dominant strategy.

The above scenario is unlikely to play out because when other people find out that extremely high rewards are being paid to the stakers, they will copy the strategy by buying and staking OHM. This is also why the percentage of OHM staked in Olympus has consistently remained over 90% since launch.
