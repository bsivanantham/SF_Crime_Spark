# SF_Crime_Spark
Spark project of Udacity's Data Stream Nanodegree

## Screenshots

### Kafka Console Consumer
**i tried to implement both in workspace and terminal. below both screenshots are there in git
![kafka-console-local](https://github.com/bsivanantham/SF_Crime_Spark/blob/master/images/kafka-consumer-console.png)
![kafka-console-workspace](https://github.com/bsivanantham/SF_Crime_Spark/blob/master/images/Terminal-%20kafakaconsusmerConsole.png)

### Spark Progress Report
![progress-report](https://github.com/bsivanantham/SF_Crime_Spark/blob/master/images/dataStrean.png)

### Spark UI
![spark-ui](https://github.com/bsivanantham/SF_Crime_Spark/blob/master/images/SparkUI.png)
![spark-ui](https://github.com/bsivanantham/SF_Crime_Spark/blob/master/images/output.png)
<a href="url"><img src="https://github.com/bsivanantham/SF_Crime_Spark/blob/master/images/output.png" align="left" height="48" width="48" ></a>

## Questions

### 1. How did changing values on the SparkSession property parameters affect the throughput and latency of the data?


I tried to use both `maxRatePerPartition` and `maxOffsetPerTrigger`. 

The lattency and throughput these two parameters. The `maxRatePerPartition` affects indiirectly(inversly propotional), `maxOffsetPerTrigger` the latency increases and the throughput decreases with decrease in the value.

Since batch always waits for previous to be completed. These Sparksessionproperty paremetes affects both latency and throughput.

### 2. What were the 2-3 most efficient SparkSession property key/value pairs? Through testing multiple variations on values, how can you tell these were the most optimal?

To increase throughput, modiy some of the default parameters like parallelism, partition, macRateperPartition and maxOffsetPerTriger. I also tried fews values to understand how it varies, best values were `maxRatePerPartition`: 300 and `maxOffserPerTrigger`: 200; There are various prossible combinations are possible to increase the `processedRowsPerSecond`