# PriceThrottler - Stage 1 (Easy)

- Time limit 30 min

You have to write a PriceThrottler class which will implement the following requirements:

1. Implement PriceProcessor interface

2. Distribute updates to its listeners which are added through subscribe() and removed through unsubscribe()

3. There is no thread-safety requirement at the moment

```java

public interface PriceProcessor {

     /**
      * Call from an upstream You can assume that only correct data comes in here –
      * no need for extra validation
      *
      * @param ccyPair
      *            - "EURUSD", "EURRUB", "USDJPY" - up to 200 different currency
      *            pairs
      * @param rate
      *            - any double rate like 1.12, 200.23 etc
      */
     void onPrice(String ccyPair, double rate);

     /**
      * Subscribe for updates Called rarely during operation of PriceProcessor
      *
      * @param priceConsumer
      *            - can be up to 200 subscribers
      */
     void subscribe(PriceProcessor priceConsumer);

     /**
      * Unsubscribe from updates Called rarely during operation of PriceProcessor
      *
      * @param priceConsumer
      */
     void unsubscribe(PriceProcessor priceConsumer);
}

```

