# Azure_AI_Anormally Detector 
 - Build an IoT Project with an Anormally detector on Stream analytics.

## Brief Description
Generally, the model's accuracy improves with more data in the sliding window. The data in the specified sliding window is treated as part of its normal range of values for that time frame. The model only considers event history over the sliding window to check if the current event is anomalous. As the sliding window moves, old values are evicted from the model's training.

The functions operate by establishing a certain normal based on what they've seen so far. Outliers are identified by comparing against the established normal, within the confidence level. The window size should be based on the minimum events required to train the model for normal behavior so that when an anomaly occurs, it would be able to recognize it.

The model's response time increases with history size because it needs to compare against a higher number of past events. It's recommended to only include the necessary number of events for better performance.

Gaps in the time series can be a result of the model not receiving events at certain points in time. This situation is handled by Stream Analytics using imputation logic. The history size, as well as a time duration, for the same sliding window is used to calculate the average rate at which events are expected to arrive.
