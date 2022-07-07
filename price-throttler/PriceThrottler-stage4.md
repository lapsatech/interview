# PriceThrottler - Stage 4 (Advanced)

- Time limit 20 min

1. Some currency pairs change rates 100 times a second and some only once or two times a day

2. ONLY LAST PRICE for each currency pair matters for subscribers. I.e. if a slow subscriber is not coping with updates for EURUSD - it is only important to deliver the latest rate

3. It is important not to miss rarely changing prices. I.e. it is important to deliver EURRUB if it ticks once per day but you may skip some EURUSD ticking every second

4. You don't know in advance which currency pair are frequent and which are rare. Some might become more frequent at different time of a day

Discuss the problems and flaws of the current solution with the given requirements. Propose solution. Update your PriceThrottler implementation according to given update

