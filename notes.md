# Chapter 1

## Contracts

 * __Forward contracts__ are one-time, have an exact delivery date,
   and have a delivery price and a price of asset at maturity,
   with the long position favoring increases in price and the short position favoring decreases.

 * __Futures contracts__ do not have an exact delivery date, and are instead restricted
   to a whole month. If a commodity is associated with the contract, it can be delivered
   on any day of that month.

## Options

 * Two basic types of options: __call options__ give the holder the right to buy
   the underlying asset by a certain date for a certain price; __put options__
   give the holder the right to sell the underlying asset by a certain date
   (the expiration date, exercise date, or maturity) for a certain price
   (the exercise or strike price).

 * __American options__ can be exercised on or before the exercise date;
   __European options__ must be exercised exactly on the date.

 * Options _may_ be exercised; contracts _must_ be exercised. Contracts are
   free, option contracts have a price.

 * If `X` is the strike price and `S_T` is the final price of the underlying
   asset, the payoff from a long position in a European call option is
   `max(S_T - X, 0)`. The payoff to the holder of a short position 
   in the European call option is `-max(S_T - X, 0)` or `min(X - S_T, 0)`. 
   The payoff to the holder of a long position in a European put option
   is `max(X - S_T, 0)` and the payoff from a short position in a
   European put option is `-max(X - S_T, 0)` or `min(S_T - X, 0). 

## Other derivative securities

 * An __interest rate cap__ provides protection against the rate of interest
   on a floating-rate loan (i.e., a high-pass filter on interest)

 * You can get very creative with derivative bundling / pricing. For example,
   __ICON__s (index currency option notes) were given out by the Long Term
   Credit Bank of Japan that yielded a bond payout less `max(0, 1000*(169/S - 1))`
   dollars, where `S` is the yen-U.S. dollar exchange rate. Thus, if 
   `S >= 169`, the full bond value is received. If `S <= 169/2 = 84.5`, then
   none of the bond value is received. In essence, this is a combination of
   a high and low-pass filter with respect to some derivative input (in this
   case, an exchange rate).

## Types of traders

 * Traders of derivative securities can be grouped into three classes:
   __hedgers__, __speculators__, and __arbitrageurs__.

 * A __hedger__ is interested in reducing the risk that they already face.
   For example, a company that must pay in a foreign currency can buy
   a long forward contract in that currency to *lock in* the exchange rate.
   The purpose of hedging is to make the outcome more certain. It does not
   necessarily improve the outcome.

   Hedging can be done using, for example, forward contracts and option
   contracts. While option contracts place a cap on the potential cost,
   they can be quite expensive.

 * While hedgers seek to reduce exposure to asset price volatility, 
   speculators take a position in the market. They are either betting 
   on or against the price of an asset in the market.

 * Arbitrageurs take advantage of instantaneous discrepancies in the market.
   For example, if the same stock is traded in New York and in London at
   `$172` and `£100`, respectively, but the sterling is trading at `$1.75`,
   then there is an arbitrage opportunity of `(1.75 * 100 - 172) = 3` dollars
   per option. If transaction costs are high (for smaller parties / transactions)
   this may not be worth it, but for large institutions with low transaction
   costs it may. In general, this situation is rare and self-correcting,
   and we assume there are no arbitrage opportunities.

# Chapter 2

## Trading

 * __Brokers__ represent other parties in a trade; __local__ represent themselves.
   
 * __Closing out__ a position involves making an opposite trade to an original one.
   For example, if an investor shorts one July contract on March 6, they can
   close out the position on April 20 by going long one July contract. The
   investor's total gain or loss reflects the change in futures price between
   March 6 and April 20.

 * For most contracts, daily price movement limits are given by the exchange.
   For example, the daily price movement limit is $1 for oil. If it moves
   a full $1 up or down it is said that the contract is *limit up* or *limit down*,
   respectively.

 * __Margins__ are used to minimize contract defaults. A __margin account__
   is the account that is used to deposit funds necessary to enter into
   a contract, the __initial margin__. The investor can withdraw excess
   of the initial margin at anytime, but a __maintenance margin__ is kept
   such that if the account decreases below the margin, a __margin call__
   is required to "top up" back to the initial margin. If the margin is not
   topped up, the broker closes out the position by selling the contract.

 * A __day trade__ is a closing out of a position in the same day.
   A __spread transaction__ is one where the trader simultaneously takes
   a long position in the contract with one delivery month and a short
   position in the contract with another delivery month.

 * An __exchange clearinghouse__ is an adjunct of the exchange and acts as
   an intermediary or middleman in futures transactions. Brokers must
   channel transactions through a clearinghouse. A clearinghouse member,
   like an individual investor, must maintain a margin account known
   as a __clearing margin__. 

 * The __gross basis__ adds the total of all long positions entered
   into by clients to the total of all the short positions entered
   into by clients. The __net basis__ allows these to be offset
   against each other. Most exchanges use net margining.

 * The point of margins and margin calls is to reduce credit risk. Outside of 
   the exchange markets, i.e., in over-the-counter markets, the equivalent
   is __collateralization__. 
  
   If the value of a contract to company A increases, then company B is
   required to pay company A cash equal to this increase. Similarly,
   if the value of the contract to company A decreass, company A is 
   required to pay company B cash equal to the decrease. Interest is
   paid on outstanding cash balances.

 * The __settlement price__ is the price at which a contract traded immediately
   before the bell signaling the end of trading for the day.

 * The __open interest__ in a contract is the number of total contracts
   outstanding. If the volume of trading in a day is greater than the
   open interest, it indicates a large number of day trades.

 * In a __normal market__, settlement prices increase as the contract
   comes to maturity. In an inverted market, the opposite occurs.

 * There are two main types of trades: commission brokers and locals.
   __Comission brokers__ are following the instructions of their clients and
   charge a commission for doing so. __Locals__ are trading on their
   own account.

   __Position traders__ (in contrast to scalpers and day traders) hold
   their positions for much longer periods of time and hope to make significant
   profits from major movements in the market.

## Orders

 * The simplest type of order is a __market order__. It is a request that
   a trade be carried out immediately at the best price available in the market.

 * A __limit order__ specifies a particular price and can only be executed
   at this price or one more favorable to the investor. For example, if
   the limit price is $30 for an investor wanting to buy, it will be
   executed only at $30 or less.

 * A __stop order__ or __stop-loss order__ also specifies a
   particular price, and is executed at the best available price once a
   bid or offer is made at that particular price or a less-favorable price.

 * A __stop-limit order__ is a combo of a stop order and a limit order.
   The order becomes a limit order as soon as a bid or offer is made at a price
   equal to or less favorable than the stop price.

   The only purpose of this is to reduce exposure to volatility in the market.
   If a stop-limit buy order is made at $40 stop and $41 limit, then as soon
   as there is sell order at $40 on the market, the first available sell
   order below $41 will be captured.

 * A __market-if-touched__ order is executed at the best available price
   after a trade occurs at a specified or more favorable than the specified price.

 * A __discretionary order__ or __market-not-held order__ is traded as a
   market order except that execution may be delayed at the broker's discretion
   in an attempt to get a better price.

 * Other types of orders are __time-of-day orders__, __open orders__,
   and __fill-or-kill orders__.

# Chapter 3 - Hedging

 * A __perfect hedge__ completely eliminates some sort of market risk, like the
   price of oil, a foreign exchange rate, the level of the stock market, or some
   other variable. 

 * A __short hedge__ involves a short position in the futures market. For example,
   if a company makes $10,000 if a given commodity goes up 1 cent, and loses $10,000
   if it goes down one cent, it could short the commodity and be certain of its
   eventual profit: the $10,000 loss per 1 cent increase and $10,000 gain per 1
   cent decrease in the commodity will offset the aforementioned loss or gain.

   A hedge has the effect of offsetting risk.
 
 * A __long hedge__ involves taking a long position in the futures market
   for hedging. It is used for when a company knows it will have to purchase
   a certain asset in the future and wants to lock in a price now.

 * Hedging is not always straightforward, since:
   
   1. The asset whose price is to be hedged may not exactly be the same
      as the asset underlying the futures contract.

   2. The hedger may be uncertain as to the exact date when the asset will
      be bought or sold.

   3. The hedge may require the futures contract to be closed out before its
      delivery month.

 * The __basis__ in a hedging situation is the spot price of the asset to be
   hedged minus the futures price of contract used. __Basis risk__ is the 
   uncertainty associated with the basis, which governs the effective price
   paid for (or sold at) of the asset being hedged (for example, if F_1
   is the current futures price of the hedged asset and S_2 and F_2 are
   its later spot and futures price, respectively, then this
   effective price is S_2 + F_1 - F_2 =  S_2 + b_2, where b_2 is defined
   as the __basis__).

 * __Cross hedging__ occurs when one asset is used to hedge a different
   asset (that may be similar in its market fluctuations).
   
 * The __hedge ratio__ is the size of the position taken in futures
   contracts to the size of the exposure. The hedger should choose a
   value of the hedge ratio that minimizes the variance of the value
   of the hedged position. 

 * The optimal hedge ratio can be shown to equal `rho * stdev_S / stdev_F`,
   where rho is the coefficient of correlation between the changes in spot
   price and changes in futures price across time (delta_S v.s. delta_F),
   and stdev_S and stdev_F are the standard deviations of these quantities.

 * The __hedge effectiveness__ is the proportion of the variance eliminated
   by hedging. This is the R^2 from the regression of delta_S against 
   delta_F and equals rho^2, or `h*^2 * stdev_F^2 / stdev_S^2`.

 * Thus, the optimal number of futures contract to hedge an asset is
   `h* Q_A / Q_F`, where h* is the hedge ratio as above, Q_A is the
   size of the position being hedged, and Q_F is the size of one
   futures contract.

 * When futures are used for hedging, a small adjustment known as __tailing
   the hedge__ is occasionally made that allows from the impact of daily
   settlement. This means replacing the quantities Q_A and Q_F above
   with V_A and V_F, the dollar value of the position being hedged and
   futures contract (the futures price times Q_F).

 ## Indices


