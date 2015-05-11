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
