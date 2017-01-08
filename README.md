# Augury
>*The practice of augury, interpreting the will of the gods by studying the flight of birds: whether they are flying in groups or alone, what noises they make as they fly, direction of flight and what kind of birds they are. [[wikipedia]](https://en.wikipedia.org/wiki/Augur)*

## Introduction
Augury is a tutorial on how to create an end to end [lambda architecture](https://en.wikipedia.org/wiki/Lambda_architecture) using [Redis](https://redis.io) as the primary data store and backbone.  It is broken into several parts that are represented as feature branches, each one implementing a different component of the architecture.  It also is an effort to highlight various use-cases for Redis in one cohesive tutorial. 

When complete, you will have the ability to garner batch and real time insights from your webserver with minimal latency impact on your running application.  You'll also have the beginnings of an analytics platform that you can use to track user behavior, generate recommendations or provide personalization.  

## Set-up
### Requirements
- Some version of Java
- Maven
- Redis
- Probably more

### Installation
- Pull the repo
- Setup dependancies
- TBD

## Sections
0. [Caching](https://github.com/timeartist/augury/tree/1-caching) - Generate a GUID that is stored for a configurable time - this is returned on a page view
0. [Session Token](https://github.com/timeartist/augury/tree/2-session-token) - Generate a GUID and a hash that is put into a cookie, store this and relevant data about it into Redis.
0. [Page View](https://github.com/timeartist/augury/tree/3-page-view) - Modify our mock page view function from part 1 to generate a click stream data object in Redis.
0. [Batch Processing](https://github.com/timeartist/augury/tree/4-batch-processing) - Create a task that reduces all click stream data into a data lake and time series data warehouse format stored in Redis on Flash.
 0. [Analytics View](https://github.com/timeartist/augury/tree/4a-analytics-view) - Create a simple view that allows the user to view aggregates of timeseries data.  Includes LUA/module scripting.
 0. [Spark Integration](https://github.com/timeartist/augury/tree/4b-spark-integration) - Put [Spark](http://spark.apache.org/) on top of the data warehouse Redis to run SQL-like queries on Redis data. 
0. [Realtime Processing](https://github.com/timeartist/augury/tree/5-realtime-processing) - Create a task that broadcasts clickstream data to a pubsub channel from a [Jesque](https://github.com/gresrun/jesque) queue.
 0. [Analytics View](https://github.com/timeartist/augury/tree/5a-analytics-view) - Generate a simple view that allows the user to see realtime data delivered from a websocket


