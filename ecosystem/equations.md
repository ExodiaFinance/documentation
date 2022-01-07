# Equations

## Staking

$$
deposit = withdrawal
$$

Swaps between EXOD and sEXOD during staking and unstaking are always honored 1:1. The amount of EXOD deposited into the staking contract will always result in the same amount of sEXOD. And the amount of sEXOD withdrawn from the staking contract will always result in the same amount of EXOD.

$$
rebase = 1 - ( exodDeposits / sEXODOutstanding )
$$

The treasury deposits EXOD into the distributor. The distributor then deposits EXOD into the staking contract, creating an imbalance between EXOD and sEXOD. sEXOD is rebased to correct this imbalance between EXOD deposited and sEXOD outstanding. The rebase brings sEXOD outstanding back up to parity so that 1 sEXOD equals 1 staked EXOD.

## Bonding

$$
bond Price = 1 + Premium
$$

EXOD has an intrinsic value of 1 DAI, which is roughly equivalent to $1. In order to make a profit from bonding, EXODIA charges a premium for each bond.

$$
Premium = debt Ratio * BCV
$$

The premium is derived from the debt ratio of the system and a scaling variable called [BCV](glossary.md#bcv). BCV allows us to control the rate at which bond prices increase.

The premium determines profit due to the protocol and in turn, stakers. This is because new EXOD is minted from the profit and subsequently distributed among all stakers.

$$
debt Ratio = bondsOutstanding/exodSupply
$$

The debt ratio is the total of all EXOD promised to bonders divided by the total supply of EXOD. This allows us to measure the debt of the system.

$$
bondPayout_{reserveBond} = marketValue_{asset}\ /\ bondPrice
$$

Bond payout determines the number of EXOD sold to a bonder. For reserve bonds, the market value of the assets supplied by the bonder is used to determine the bond payout. For example, if a user supplies 1000 DAI and the bond price is 250 DAI, the user will be entitled 4 EXOD.

$$
bondPayout_{lpBond} = marketValue_{lpToken}\ /\ bondPrice
$$

For liquidity bonds, the market value of the LP tokens supplied by the bonder is used to determine the bond payout. For example, if a user supplies 0.001 EXOD-DAI LP token which is valued at 1000 DAI at the time of bonding, and the bond price is 250 DAI, the user will be entitled 4 EXOD.

## EXOD Supply

$$
EXOD_{supplyGrowth} = EXOD_{stakers} + EXOD_{bonders} + EXOD_{DAO}
$$

EXOD supply does not have a hard cap. Its supply increases when:

* EXOD is minted and distributed to the stakers.
* EXOD is minted for the bonder. This happens whenever someone purchases a bond.
* EXOD is minted for the DAO. This happens whenever someone purchases a bond. The DAO gets the same number of EXOD as the bonder.

$$
EXOD_{stakers} = EXOD_{totalSupply} * rewardRate
$$

At the end of each epoch, the treasury mints EXOD at a set reward rate. These EXOD will be distributed to all the stakers in the protocol.

$$
EXOD_{bonders} = bondPayout
$$

Whenever someone purchases a bond, a set number of EXOD is minted. These EXOD will not be released to the bonder all at once - they are vested to the bonder linearly over time. The bond payout uses a different formula for different types of bonds. Check the bonding section above to see how it is calculated.

$$
EXOD_{DAO} = EXOD_{bonders}
$$

The DAO receives the same amount of EXOD as the bonder. This represents the DAO profit.

## Backing per EXOD

$$
EXOD_{backing} = treasuryBalance_{stablecoin} + treasuryBalance_{otherAssets}
$$

Every EXOD in circulation is backed by the EXODIA treasury. The assets in the treasury can be divided into two categories: stablecoin and non-stablecoin.

$$
treasuryBalance_{stablecoin} = RFV_{reserveBond} + RFV_{lpBond}
$$

The stablecoin balance in the treasury grows when bonds are sold. [RFV](glossary.md#rfv) is calculated differently for different bond types.

$$
RFV_{reserveBond} = assetSupplied
$$

For reserve bonds such as DAI bond, the RFV simply equals to the amount of the underlying asset supplied by the bonder.

$$
RFV_{lpBond} = 2sqrt(constantProduct) * (\%\ ownership\ of\ the\ pool)
$$

For LP bonds such as EXOD-DAI bond, the RFV is calculated differently because the protocol needs to mark down its value. Why? The LP token pair consists of EXOD, and each EXOD in circulation will be backed by these LP tokens - there is a cyclical dependency. To safely guarantee all circulating EXOD are backed, the protocol marks down the value of these LP tokens, hence the name _risk-free_ value (RFV).
