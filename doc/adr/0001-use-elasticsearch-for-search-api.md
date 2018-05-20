# 1. Use Elastic Search for exposing enterprise wide search API.

Date: 2018-05-20

## Status

Accepted

## Context

There is a need of having an API exposed which can be used to search enterprise wide common data model.

The data currently resides in a RDBMS database, it is difficult to expose micro-services directly querying out of RDBMS databases since the application runs out the same environment. 

There are options like ElasticSearch or Solr where data can be replicated.  

## Decision

Use ElasticSearch for data indexing

## Consequences

Data needs to be replicated across the ElasticSearch cluster. This separate cluster needs proper maintenance. 

 * Near-real time data replication is required.
 * Additional cost of maintaining the ElasticSearch environments

