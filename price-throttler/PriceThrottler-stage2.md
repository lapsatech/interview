# PriceThrottler - Stage 2 (Easy)

- Time limit 15 min

Some subscribers can handle only specific currency pairs

Update your PriceThrottler implementation according to this information

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
      * @param priceProcessor
      *            - can be up to 200 subscribers
      */
     void subscribe(PriceProcessor priceProcessor);

 

     /**
      * Unsubscribe from updates Called rarely during operation of PriceProcessor
      *
      * @param priceProcessor
      */
     void unsubscribe(PriceProcessor priceProcessor);

 

     /**
      * Reports currency pair names that processor can handle
      *
      * @return array of currency pair names or null. Null means that the
      *         PriceProcessor is able to handle any currency pair
      */

     String[] getProcessCcyPairs();

}

```
