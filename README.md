# SF_Crime_Spark
Spark project of Udacity's Data Stream Nanodegree

## Screenshots

### Kafka Console Consumer
![kafka-console-local](https://github.com/bsivanantham/SF_Crime_Spark/blob/master/images/kafka-consumer-console.png)
![kafka-console-workspace](https://github.com/bsivanantham/SF_Crime_Spark/blob/master/images/Terminal-%20kafakaconsusmerConsole.png)

### Spark Progress Report
![progress-report](https://github.com/bsivanantham/SF_Crime_Spark/blob/master/images/dataStrean.png)

### Spark UI
![spark-ui](https://github.com/bsivanantham/SF_Crime_Spark/blob/master/images/SparkUI.png)
![spark-ui](https://github.com/bsivanantham/SF_Crime_Spark/blob/master/images/output.png)

## Questions

### Question 1

I tested `maxRatePerPartition` and `maxOffsetPerTrigger`. 

When we increase the value of `maxRatePerPartition` the latency drops and the throughput increases.

When we decrease the value of `maxOffsetPerTrigger` the latency increases and the throughput decreases.

These answers were evaluated `inputRowsPerSecond` and `processedRowsPerSecond`

### Question 2

Best values:

    * `maxRatePerPartition`: 300;
    * `maxOffserPerTrigger`: 200;

These are the values that give higher `inputRowsPerSecond` and `processedRowsPerSecond`. I have also evaluated if these metrics were similar, meaning we can process the same amount of data that arrives.