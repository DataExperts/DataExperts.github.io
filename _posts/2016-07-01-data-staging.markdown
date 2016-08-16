---
layout: post
title:  "The importance of staging data"
date:   2016-07-01 18:00:00 +1000
author: Gary Holland
summary: What is data staging, and why should it be an integral part of an organizations information management strategy?
categories: updates
---

What is data staging, and why should it be an integral part of an organizations information management strategy?

Data Staging
---

A data staging environment is an effective way for an organization to quickly improve its data maturity by reducing redundancy and building a one-stop-shop data resource.  

In the past [data warehouses](https://en.wikipedia.org/wiki/Data_warehouse) and [ODS's](https://en.wikipedia.org/wiki/Operational_data_store) (operational data stores) have been touted as the one-stop-shop for maintaining data in the enterprise.  However, time has proven many times over that maintaining an entire organizations data in a data warehouse with continuously changing applications, regulations, mergers/de-mergers, diverse lines of business and high volumes of data has proven virtually impossible.  The net result is that many maintain multiple data warehouses, which are expensive, and serve only very specific reporting and regulatory needs.  This high cost and complexity of them often drives new projects to avoid the data warehouses, and this is causing an explosion of data silos in the enterprize.  

Data proliferation within the enterprise is not just an inconvenience.  A recent assessment by Veziron determined that at least [80% of organizations](http://news.verizonenterprise.com/2015/03/verizon-2015-pci-compliance-report/) fail to meet their [PCI/DSS](https://en.wikipedia.org/wiki/Payment_Card_Industry_Data_Security_Standard) compliance obligations, leaving them vulnerable to cyber-attacks.  The number of data breaches is increasing dramatically with the Privacy Rights Clearing House recording over [900 million breached records](https://www.privacyrights.org/data-breach) that have been made public since 2005.

Recent technologies such as [Big Data](https://en.wikipedia.org/wiki/Big_data) (e.g. Hadoop, NoSql databases, cloud stores) and frameworks such as [Data Lakes](https://en.wikipedia.org/wiki/Data_lake) have delivered capabilities  that can deal with large data volumes of virtually any structure.  For data scientists and organizations looking to find 'needle in the haystack' types of insights, these technologies have been a gold mine.  The pitfall of these technologies is that enterprize's are quickly creating [data graveyards](http://www.pwc.com/us/en/technology-forecast/2014/cloud-computing/assets/pdf/pwc-technology-forecast-data-lakes.pdf) and losing track of the data.  

Organizations often skip staging data in favor of point-point interfaces when delivering data to data warehouses or other applications.  These interfaces are often built for specific requirements and cherry pick the fields and datasets as needed.  Tactically this might seem like a quick and efficient approach, however when subsequent projects requires similar data, they will need to build additional interfaces.  Before  long there become a complex, costly and unmanageable set of spaghetti looking interfaces.  


A data staging framework, can provide some balance by being low cost to maintain and allowing high volumes of any types of data, whilst still time allowing auditing, security, and data lineage capabilities.  This will provide the following benefits:

* Provides a secure central resource that can be encrypted and access rights set globally.
* Reduces data redundancy.
* A reusable data resource for projects, data analysts and scientists. 
* Enable data lineage so all data can be traced to source systems and owners and where it delivered to.

The key attributes of a data staging environment are:

* **Raw Format** - Data are stored in a raw format, meaning the data are structured in the same manner as the system that it was sourced from.
* **Parallel Loads** - There should be no dependencies (such as foreign keys) between tables to ensure data loads can be run in parallel and optimized with bulk processing.
* **Avoid data cleansing** - Exceptions to this rule might be simple filters to remove junk rows and columns.
* **Encrypt Sensitive Data** - Sensitive data fields should be either excluded, encrypted or hashed.  
* **Preserve History** - Where practical change history should be retained which allows queries that can see how the source table looked at any point in time.  Exceptions to this rule, might be due to privacy regulations or volume constraints.
* **Includes Auditing & Tracing** - Auditing columns should be added to the staging tables to allow tracing of data back to the source system and data/time the data was created and updated.  This is critical for understanding data, and also help ensure compliance with regulations (such as Sarbanes Oxley).
* **Catalog and Document** - Tables should describe the data and where it came from as well as linking to data owners and other stakeholders responsible for this data.

The [Data Experts Information Hub](http://dataexpertsgroup.com) is built around a best-practice framework that incorporates data staging with the attributes described in this paper.  