---
title:  Terracotta 10.7 Release Notes  
lang: en
layout: page
keywords:
space: release
sidebar: lb2_sidebar
permalink: /display/release/Terracotta+10.7+Release+Notes.html
summary:
---

Terracotta is a distributed in-memory data management solution for both operational storage and analytical processing.  Terracotta has powerful query and computation capabilities, leveraging native JDK features such as Java Streams, collections, and functions. It supports the following sub-systems:

*   A storage sub-system fronted by TCStore API
    
*   A caching sub-system fronted by the next generation Ehcache API which includes and extends JSR 107
    

Both sub-systems are backed by the distributed Terracotta Server, which provides a common platform for distributed in-memory data storage with scale-out, scale-up and high availability features.



* TOC
{:toc}

# Feature Highlights
------------------

The Terracotta 10.7 release builds upon the enterprise readiness features and analytical capabilities of past releases, by improving operational usability and performance. Some of the notable features of Terracotta 10.7 include:

*   Significant replacement of the configuration system of Terracotta Servers
*   Improved ability to scale-out (horizontally) servers without downtime
*   Formal support for complex data types in TCStore

# Summary of Changes 10.7
-----------------------

### New in Terracotta 10.7.0.0 and 10.7.0.1 

*   Dynamic Cluster Configuration
    *   Terracotta Servers are no longer configured via XML configuration files (difficult to keep consistent across servers in the cluster, requiring reloading for changes to take affect)
    *   Terracotta Servers are now configured with "config-tool" which opens the door to more dynamic to changes of configuration across the cluster.
*   Improved ability to scale-out (horizontally) servers without downtime  
    *   Use config-tool to add or remove stripes from clusters
*   Formal support for complex data types in TCStore  
    *   New Cell types:  Map and List (which can each contain Maps and Lists)
*   Azul Java 11 Support
*   DSL support for constant functional expressions in TCStore

####       Resolved

*   4674 - close() is blocked when servers are gone if entity.close() is called.
*   4767 - Performance overhead when adding new cell definition in each record of a Dataset.
*   4720 - Cell data omitted when too many CellDefinitions used in Dataset.
*   4783 - Three node stripe data loss scenario possible during passive connection.

####      Security Updates to Third Party Libraries

*   5317 - jackson-databind updated to 2.10.5.1 (CVE-2020-25649)
*   5234 - snakeyaml updated to 1.26 (CVE-2003-1564)
*   Various other 3rd party library updates

  

# Notes:
------

*   Terracotta BigMemory 4.x and Terracotta 10.x clients may be used simultaneously in the same application by ensuring ClassLoader isolation when initializing at least one of the clients.

  


