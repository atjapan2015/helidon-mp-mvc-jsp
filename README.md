
# Helidon JSP MP Example

This is under developing so it's not working now.

This example implements a simple Hello World Web Application using Helidon + MicroProfile + JSP

## Prerequisites

1. Maven 3.5 or newer
2. Java SE 8 or newer

Verify prerequisites
```
java -version
mvn --version
```

## Build

```
mvn package
```

## Start the application

```
java -jar target/helidon-mp-mvc-jsp.jar
```

## Exercise the application

http://localhost:8080/web/index

## Try health and metrics

```
curl -s -X GET http://localhost:8080/health
{"outcome":"UP",...
. . .

# Prometheus Format
curl -s -X GET http://localhost:8080/metrics
# TYPE base:gc_g1_young_generation_count gauge
. . .

# JSON Format
curl -H 'Accept: application/json' -X GET http://localhost:8080/metrics
{"base":...
. . .

```
