Lets imagine the situation.

You have a trade system that generates currency exchange prices for a number of currency pairsm for example eg USDGBP, USDEUR. There can be up to 200 pairs in total.
Lets call it upstream.

In the other hand we have a lot of downstream systems that wants to receive these price rates.

But the issue is that our trade system can work with the single downstream recipient only. This is by design and we can't do anything about that. Lets image this is a kind of legacy system we have no access to source code to.

So namely this upstream can work with the single PriceConsumer implementation.

So the task is to write the class with the name PriceThrottler that will be implementing PriceConsumer interface. 

The instance of that class will be that single  recipient for our upstream and all our downstream systems will be considered as subscribers for the PriceThrottler instance.
