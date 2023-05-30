# Azure_AI_Anormally Detector 
 - Build an IoT Project with an Anormally detector on Stream analytics.

## Brief Description
Generally, the model's accuracy improves with more data in the sliding window. The data in the specified sliding window is treated as part of its normal range of values for that time frame. The model only considers event history over the sliding window to check if the current event is anomalous. As the sliding window moves, old values are evicted from the model's training.
