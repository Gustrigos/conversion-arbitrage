# conversion-arbitrage
- Analyzing the behavior of Berkshire Hathaway's common stock class A and B to find conversion arbitrage opportunities at times of maximized spreads. 

#### Background

In 1996 Berkshire Hathaway Inc. issued Class B shares at one-30th of the price of Class A shares. In 2010 a 50-1 stock split diluted the ratio to one-1500th. 

### Share Price
Class B shares can never sell at less than one-1500th of the price of Class A. When Class B shares price rise above the one-1500th fraction, arbitrage takes place (Buffet, 1999). For this, a specialist buys the Class A and converts it into Class B, which pushes the prices back to the one-1,500th ratio. Class B, however, can sell for less than one-1500th of the price of Class A since conversion does not happen the other way around.  When there is more demand for for Class B than Class A relative to their supply, Class B will sell at one-1,500th of the price of Class A. But when there is less demand, Class B will be at discount. 

Buffett's take: in his 1999 memo to all his investors, Warren Buffet recommends: “when the [Class]B is at a discount of more than say, 1%, it offers a better buy than the A. When the two are at parity, however, anyone wishing to buy 1,500 or more B should consider buying A instead.” (Berkshire Hathaway, 2017). 

## Voting Rights
As of May 5th 2018, Class A stock is entitled to one vote per share and Class B Stock is entitled to one-ten-thousandth (1/10,000) of one vote per share. 

## Convertibility
Each share of a Class A common stock is convertible at any time, into 1,500 shares of Class B common stock. However, the conversion privilege only applied to Class A shares, which does not extend the ability of Class B shareholders able to convert to Class A. 

# Arbitrage Opportunity
## Preamble
Class A and Class B behave similar and should have the same return over time. This is due because Class B was issued (and derived) from Class A. Class A's last dilution made Class B have a price ratio of one-1500th. Therefore, if the adjusted close of Class B is multiplied by a factor of 1,500, it’s real price should be equal to that of Class A at a given date.

Nevertheless, one of the main factors that makes Class B differ from Class A is its liquidity. Because Class B is much more affordable and accessible to a broader group of investors, Class B does not bear the amount of liquidity premium that Class A has to compensate its illiquid state. Consequently, small divergences between each stock happen. This opens up the opportunity of arbitrage within a small time frame. In his investor’s Memo in 1999, Warren Buffett explains thatthe arbitrageur will only have the chance to catch the opportunity only if he is a holder of Class A. However, he explains, as soons as he converts Class A, the market will efficiently balance out again, and mitigate the divergence between Class B.

## Assumptions
In this analysis, I wanted to understand quantitative methods to find arbitrage opportunities within Class A and Class B and use technical analysis graph methods to find opportunities of arbitrage assuming the holder has Class A stocks. For this, I make up initial assumptions to have a theoretical overview of the arbitrage opportunities on conversion strategy: 1) I assume there is no transaction cost, 2) I assume the stockholder owns 50 Class A stocks, 3) While I am utilizing intraday data, I assume the arbitrageur transacts within a fast time frame and wants to maximize it’s return by catching maximal spread. 

## Methodology
Initially, I obtained the adjusted closing for Class A and Class B and scaled Class B by a factor of 1,500. Then, I computed the ratio between Class A and the adjusted Class B, where it explained whether the prices of both stocks are fairly priced (ratio of 1), or if there was any arbitrage opportunity (when the ratio is smaller than 1, and Class B is overpriced).

The arbitrage opportunity arises when Class A holders convert their shares from A to B when the ratio is smaller than 1, and then sells all their Class B stocks immediately.

For this use-case, I chose the single back-tested datapoint with the maximal spread whitin an in-sample period of 7 years with a direction smaller than the fair price ratio of 1. In this case, we chose the lowest ratio after 2010’s January 21st Class B stock split, which happened in February 12 2010 at a ratio of 0.9882965.

## Conversion
With the assumption of holding 50 stocks of Class A in February 12 2010, at adjusted closing price of $114,000, and the investor able to see a spread in the fair price ratio below 1 of 0.9882965, a conversion from Class A’s price to Class B will output an instant return of 1.18421% if once converted, sold at the price of Class B. Considering the 50 stocks of Class A, with a total equity of $5,700,000, the conversion would dilute the investor but give it the equivalent of 50 Class A stocks multiplied by a factor of 1500 to 75,000 stocks of Class B at the current overpriced price. If the investor sold right away, his or her equity would increase from $5,700,000 to $5,767,500 or a difference of $67,500, which represents the net profit gained from the arbitrage.

## Takeaways
Regardless of the theoretical profit on the conversion, applying this arbitrage in real life bears flaws that makes arbitrage opportunity virtually unfeasible. Class A is market illiquid, a conversion will move significant volume from one class to another, which will make Class B’s price reverse back to their fair price ratio almost immediately, negating the spread between both Class A and Class B scaled prices. 

