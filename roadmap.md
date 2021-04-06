# Roadmap

### Leverage trading and short selling for synthetic assets

We believe this will be one of the most important features of MarsSwap. If you think an asset is going up, you can increase your exposure to magnify the returns. On the other hand, if you believe the asset is going down, you will be able to short it and profit from it.

In order to implement this feature, we will use a system of lending and borrowing. Like in other lending platforms, to protect the lender’s assets, borrowers must keep a collateral on MarsSwap. But maintaining unused collateral might not be ideal for investors. For this reason, we will support the use of tokens staked on farms or pools as collateral. Your collateral will generate rewards while you are free to use your borrowed assets.

Leverage and short selling might be used for speculative reasons but also to **hedge against impermanent loss**.

### Option derivatives for synthetic assets

Options trading has gained a lot of popularity in recent years. The same lending and borrowing functionality implemented for leverage trading can be used for implementing options. MarsSwap protocol will allow users to buy calls and puts on any of the supported synthetic assets. We will likely start by offering standardized expiration dates, and over time extend to more customizable derivatives.

### Integration with popular dex aggregators

Unlike many PancakeSwap clones, we implemented our own AMM exchange with custom routing capabilities. This makes it possible to trade cross-assets using MARS as a bridge. For example, an investor can swap mFB for mTSLA in an atomic transaction, in which the MarsSwap protocol will connect the MARS-mFB and MARS-mTSLA liquidity pools.

This capability makes it attractive for decentralized exchange aggregators to integrate with our router. Dex aggregators will benefit from high liquidity between synthetic assets, while MarsSwap’s liquidity providers and MARS holders will benefit from every transaction on these exchanges. We plan to integrate with 1inch and autofarm as soon as we meet the minimum liquidity requirements.

### Leveraged farming

Using the same lending and borrowing features implemented for leverage trading, we can support leveraged farms. These farms will increase the exposure to both a farm’s reward and price movements of the staked tokens. On the other hand, for more risk-averse users, MarsSwap will offer farms with smaller APRs but with a built-in hedge against impermanent loss.

### Limit orders

Limit orders on MarsSwap protocol will allow submission, updates, and execution of buy and sell orders at a limit price specified by the users. Once the limit order is submitted and the limit price is reached, market-making agents will be able to read the orders from the Limit Order contract and execute them when it provides an arbitrage opportunity.

### Stop Loss and Take Profits

SL and TP are critical functionality for reducing the risk on any trading platform. Still, decentralized exchanges have generally not offered these features. Executing transactions on-chain as a response to events like price movements is not straightforward. MarsSwap protocol will solve this by taking a small fee when the SL or TP is triggered. This fee will be used to reward market participants who close these positions when the thresholds have been reached. The functionality will be embedded into the smart contract, allowing anyone to monitor and profit from closing operations.

####  

