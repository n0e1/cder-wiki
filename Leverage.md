CDER.IO offers leverage on operations with derivatives. Maximum leverage is x25. Be careful - high leverage increases trading risks.

To open a position, you need to have a sufficient initial margin level which serves as a collateral for your order. It is calculated in proportion to the leverage you choose. For example, initial margin for leverage x2 is 50% of the order amount; initial margin for leverage x10 is 10% of the order amount; for leverage x 25 you need to deposit only 4% of the order amount. After your order is executed, 30% of the initial margin will be transferred to you Margin Balance. This amount will be automatically used to maintain your positions, or you can use it to place new orders or transfer it to your account.

If you do not want your position to be liquidated, you need to have a sufficient maintenance margin level. What does it consist of?
<ul>
<li>70% of the initial margin for your order</li>
<li>Margin Balance, including 30% of the initial margin for your order</li>
</ul>

If your position exceeds maintenance margin, it will be liquidated. 

CDER.IO uses a cross margin method. This means that the maintenance margin level of your Margin Balance will be shared between all your open positions. Therefore, when a trader has several open positions, the level of the maintenance margin also includes:
<ul>
<li>Unrealized positive PNL on all open positions</li>
</ul>

> Example:
> 
> A trader is long 100 fX contracts, 1 ETH each. A trader is also long 100 fY contracts, 1 ETH each. In total, it is 200 ETH. Leverage for both positions is x10. This means that the amount of initial margin is 10 ETH for each position. The trader has reserved 20 ETH for placing two orders. At the same time, when the orders were executed, 30% of the initial margin, i.e. 3 ETH (6 ETH in total), was transferred to the trader’s Margin Balance. Liquidation price for each position will be calculated as follows:
> <ul>
> <li>70% of the initial margin for the order - 7 ETH </li>
> <li>Margin Balance, i.e. 30% of initial margin for both positions - 6 ETH</li>
> <li>Other funds in the Margin Balance</li>
> </ul>
> Thus, when a trader opens a position on such terms, the position liquidation price will be calculated based on the maintenance margin - 13 ETH. Maximum reduction in the position value is 13%.
> 
> In our example, if one of the positions - fX - grows by 20%, then unrealized positive PNL on the first position will be used for calculating liquidation price for the second position:
> <ul>
> <li>unrealized positive PNL on the fX position is 20% of 100 ETH, i.e. 20 ETH</li>
> </ul>
> 
> Then the liquidation price for the second position is 7 ETH (70% of the initial margin for the order) + 6 ETH (Margin Balance - 30% of the initial margin) + 20 ETH (unrealized positive PNL on the other position) = 33 ETH. In this case, the maximum reduction in the second position value is 33%.

 

### Margin Balance

Margin Balance is designed to maintain existing positions with leverage. Margin Balance automatically maintains those positions that are close to liquidation. You can always top up your balance in a separate window, or withdraw your funds. However, if part of the balance is used to maintain open positions, you can only withdraw uncommitted funds.

Margin Balance is formed based on:
<ul>
<li>direct top up from your wallet</li>
<li>gas price rebate when you place an order as a maker and cancel orders</li>
<li>realized PNL after closing positions</li>
</ul>

### Liquidation Process

If your funds are sufficient to maintain your positions, they might be liquidated. Fair Price Marking system is used to calculate liquidation price. It allows to avoid artificial liquidation when price outliers occur as a result of market manipulations. If traders cannot fulfill their maintenance requirement, they will be liquidated. 
