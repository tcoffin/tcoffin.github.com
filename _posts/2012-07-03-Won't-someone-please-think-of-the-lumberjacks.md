---
layout: post
title: Won't someone please think of the lumberjacks!
---
### Why does your software produce logs?  
There are many applications that produce a debug log of statements that the developer has inserted for their own _debugging_ purposes, those logs are irrelevant to this discussion since they're basically not intended to be used in production.  
However if the logs are there for production purposes (regulatory compliance, workflow traceability, production troubleshooting, etc.) then it is quite reasonable to expect that someone or something will need to read those logs. This is the majority of the cases (otherwise, why bother) therefore you should really make sure that your logs are actually useful.  
Some tips for logs:  
- Parseable! - Definite a consistent format and stick to it. Use separators between the fields. Pro tip: ASCII code 0x1e is a whitespace character designed for separating records.  
- _complete_ timestamps - Year all the way down in resolution to second (or better if you can!). If its server software, including the timezone or having it in UTC is important too. Consider [RFC3339](http://www.ietf.org/rfc/rfc3339.txt) timestamps; they give you everything you need in an easy to parse format. Also, this should be first thing on every log line because it makes it easy to merge and sequentially sort your logs!
