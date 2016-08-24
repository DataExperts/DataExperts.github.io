---
layout: post
title:  Introducing the Information Hub
date:   2016-08-03 10:06:01 +1000
author: Gary Holland
summary: Learn about the integration hub and how it will support your information strategy.
categories: updates
---

The Integration Hub is our online platform that enables users to manage their data.  This paper is a quick start and is intended to provide an overview of how the Hub works.

Concept 1: Remote Agent
---
The remote agent is a lightweight executable package that is remotely controlled by the Integration Hub website.  This is run locally on the network where the resources are located (such as database and network drive). To build data integration jobs at least one remote agent needs to be running.

Remote Agents are supported on the following platforms:
|Platform|Comments|
|---|---|---|
|Windows|Requires .Net Framework 4.6 or standalone install on Windows 7/8/10.| 
|Mac|||
|Linux|Ubuntu 14.4/16.4| 
|---|---|---|

Concept 2: Data Points
---
Data Points are connections or pointers to data.  Data ponts can reference databases, web services, or delimited files.  

There are three discrete type of data points that are used in the Integration Hub:

|Data Point|Details|Types of Data|
|---|---|---|
|Source|Where the source data is located.  Source data points are used for extracting data, and only require read access to function.|Sql Databases, NoSql Databases, Web Services, Delimited Flat Files|
|Managed|Database used by the integration hub to store and publish data.  The integration hub requires full access (i.e. create/update/delete tables) to the managed database, and generally the database exclusively used by the integration hub.|Sql Databases, NoSql Databases.|
|Target|Target data points are areas where the integration hub can deliver data to.  The integration hub will require some access privileges to insert/update/delete table records, and can optionally create the tables in the target.|Sql Databases, NoSql Databases (Azure Table Storage), Delimited Flat Files.|
|---|---|---|

Currently the following connections are supported by data points:

|Category|Connection Type|Comments|
|---|---|---|
|Sql Database|Sql Server|current support for Sql Server 2012-2016.|
|Sql Database|Sqlite||
|NoSql Database|Azure Storage Table|Requires an Azure account|
|Delimited|Local Storage|Delimited files on local or network drives|
|Delimited|Azure File Storage|Delimited files stored on Azure File Storage (note, requires Microsoft Azure account)|
|Web Service|Soap based|Only supported when running remote agent on Windows system|
|Web Service|Rest based|Currently supports open and token based web services, OAuth support coming soon|
|---|---|---|

Planned:  Final release plans will include connectivity to Oracle, MySQL databases.  

Concept 4: Data Tables

Data Tables are metadata representations of relational tables or other data sources.  The metadata in data tables is important in driving the data integration process.

The following metadata is contained in a data table.

|Property|Purpose|Comments|
|---|---|---|
|Table Name|Reference to underlying table.||
|Logical Name|A simple short name to the table.  This does not need to match the underlying table.||
|Description|A description of the table.||
|Description|A description of the table.||


Concept 3: Data Links
---

Data Links are objects

|Data Category|Details|
|---|---|
|Staging Data|Raw source data that has been consolidated centrally.|
|Validated Data|Data which has been through a cleansing and validation process, with poor quality data either being cleaned or filtered and rejected.
|Rejected Data|Data which failed validation and has been put aside in a rejected table.
|Transformed Data|Data which has been through some sort of transformation process.  Transformation processes can include mapping fields, aggregating or grouping data, joining data, running business rules and analytical processes.  
|Profile Data|The results of a data profiling process
|Audit Data|The results of any data link executions, including rows processed, performance, and duration.
