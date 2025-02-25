---
title:  Platform Support Terracotta 3.6, Ehcache 2.5, Quartz 2.1  
lang: en
layout: page
keywords:
space: release
sidebar: lb2_sidebar
permalink: /display/release/Platform+Support+Terracotta+3.6%2C+Ehcache+2.5%2C+Quartz+2.1.html
summary:
---

* TOC
{:toc}

Platform Support
================

The platforms listed on this page are currently certified for use with commercial Terracotta product editions. As a 100% Java solution, Terracotta should run without issues on Java platforms for which it is not certified. If you have any questions about a certified or non-certified platform, contact us in one of the following ways:

*   Send email to [info@terracotta.org](mailto:info@terracotta.org)
*   Post a question on our [community forums](http://forums.terracotta.org)

Terracotta is comprised of two different components: the **client** that integrates with your application, and the **server** (the server array) that typically runs on a set of separate machines in production.

The client is designed to run on many platform/JDK/container combinations. The server runs directly as a Java process (without a container).

Client JDKs
===========

For standard usage (also referred as Express integration) - via standard application libraries - with Ehcache, Quartz and Web Sessions, the following JDK's are supported:

| JDK Version |
| --- |
| Sun Hotspot 1.5.0\_22 |
| Sun Hotspot 1.6.0\_30 |
| Oracle BEA JRockit 1.6.0\_26-b03 R28 |
| IBM JDK 1.5 |
| IBM JDK 1.6 |

Custom/DSO Usage

*   In addition to the ability to integrate Terracotta via standard application libraries (Ehcache, Quartz and Web Sessions), Terracotta also supports a Custom/DSO (Distributed Shared Objects) integration mode. Custom/DSO provides support for additional advanced use cases via lower level JVM-level data type clustering. It is typically only used for direct JVM-level POJO clustering (without using Ehcache), or uses cases that combine Ehcache with explicit DSO clustering of other data types in a single application, or when using Ehcache in non-serialized identity mode.
*   For more information on integration and installation modes, see our
    
*   Custom/DSO usage is only supported with the Sun Hotspot JDK - as it relies on a JDK specific boot-jar for byte-code manipulation. Additionally, Websphere is not support with Custom/DSO usage.

Client Containers
=================

| Container Version |
| --- |
| Apache Tomcat 7.0.16 |
| Apache Tomcat 6.0.29 |
| Apache Tomcat 5.5.28 |
| Apache Tomcat 5.0.30 |
| IBM Websphere 6.1.0.25 |
| IBM WebSphere 7.0.0.9 |
| JBoss AS 4.0.5 |
| JBoss AS 4.2.3 |
| JBoss AS 5.1.0 |
| JBoss AS 6 |
| Jetty 6.1.15 |
| Jetty 6.1.26 |
| Jetty 7.4.4 |
| Oracle BEA Weblogic 9.2.MP3 |
| Oracle BEA Weblogic 10.0 MP1, MP3, 10.3.1 |
| \* Glassfish V2-ur2-b04 |
| \* Glassfish V3 |
| \* Resin 3.1.8 |

\* Indicates - supported for Ehcache, Quartz, but not Web Sessions. Contact to [info@terracotta.org](mailto:info@terracotta.org) for availability.

Server Information
==================

The Terracotta server is a process that runs directly in a JVM.  
It has been validated on the following OSes with Sun Hotspot JDK 1.6.0\_27

*   Solaris 10(SPARC)
*   Solaris 9(SPARC)
*   RedHat ES4
*   RedHat ES5
*   SUSE ES 10.1 32 and 64 bit
*   Windows Server 2003 R2
*   Windows XP (dev only)
*   Windows Server 2008R2
*   CentOS 5.4

For other JVM/platform combinations not listed above, please contact info@terracotta.org to confirm status.

Library to Server Compatibility Matrix
======================================

[Library+to+Server+Compatibility+Matrix](Library+to+Server+Compatibility+Matrix)

If you are using Sun SPARC, see the [SPARC section of the Troubleshooting Guide](/display/docs/Troubleshooting+Guide).

For Terracotta Server garbage-collector settings, see the [Technical FAQ](Technical+FAQ).


