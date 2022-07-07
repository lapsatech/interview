# PriceThrottler - Stage 3 (Advanced)

- Time limit 20 min

1. Some subscribers are very fast (i.e. onPrice() for them will only take a microsecond) and some are very slow (onPrice() might take 30 minutes).

Imagine that some subscribers might be showing a price on a screen and some might be printing them on a paper

2. Slow subscribers should not impact fast subscribers

3. You don't know in advance which of the subscribers are slow and which are fast. Is there any issues you see with your current implementation taking into account new incoming requirements? How do you propose to solve it? Discuss your solution with the interviewer. Update your PriceThrottler implementation according to given update.

