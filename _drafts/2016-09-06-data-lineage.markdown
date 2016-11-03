---
layout: post
title:  "Building an auditable data framework"
date:   2016-07-01 18:00:00 +1000
author: Gary Holland
summary: Building an "auditable" data environment is the most important tenant of an effective information management strategy. 
categories: updates
---

## The rational for building auditable platforms

After 20 plus years of working with clients and personally experiencing the pain of not being able to understand data left by previous projects, my view is that building auditability into the core design of any technology platform is **literally** the most important design component to put in place if you care about managing data efficiently over a long period of time.  

I didn't always have this view.  I started my career in the mid 1990's as a Business Intelligence consultant, where I was involved with a number of data warehouse projects.  With these projects, we would usually be start with a mock set of reports required by the business, we'd then extract and load data from where ever we could find it into empty databases.  The sources were a combination of extracts from ERP systems, spreadsheets, and mainframes, which we automated by building database scripts and c programs.  As we started each new requirement with a clean slate, we delivered data warehouses and reporting quickly, and at the time were highly praised for the results we produced.  Fast forward 20 years, and the result of this approach being repeated over has left many organizations with hundreds of siloed legacy systems they don't understand, are afraid to touch, and are hopelessly out of date.  

Auditability is a form of insurance.  In 2012 the RBS(Royal Bank of Scotland) updated their payment processing system which resulted in a major [fault](https://en.wikipedia.org/wiki/2012_RBS_Group_computer_system_problems).  This  impacted customers for weeks, with some unable to purchase houses, others stranded overseas and many not paid or able to access ATM's.  The bank was fined £56m over the incident, and other financial and reputational costs are estimated to be in the billions of pounds.  With strong auditing controls in place, the risk of this type of incident can be massively reduced, and if it does occur staff are in a better position to understand and correct unexpected data corruptions.

A common misnomer is that it's hard work to build a platform that is auditable.  The truth is, if included in the initial design and tooling it should only add a small effort, which will be repaid quickly as the project will now be able to quickly adapt to change and provide a valued asset that can be leveraged by future projects.  The real challenge with auditing is trying to retrofit it into previous projects.  This can be very expensive, and in many cases a rebuild of the platform can be simpler.

Some additional rational for implementing an auditable platform are:

* **Securing Data** - If you don't understand your data, who owns it and where it (or copies of it) reside, you can be exposed when it comes to securing it.  A 2014 [EMC survey](http://www.securityweek.com/downtime-and-data-loss-cost-enterprises-17-trillion-year-emc) over 3,000 decision makers across suggested a loss of $1.7 trillion in data loss, with the volume of data increasing at 400% in the last two years.  The alternative, which is to aggressively lock down all data is not great either, as it restricts employees ability to legitimately leverage data when they need it.
* **The Next Project** - Virtually every project in an organization is challenged to deliver more for less.  However, when projects consume and create new data without appropriate auditing capabilities, they are effectively creating a technology debt (or backlog) that some future project will have to fix.  The **next** project that uses similar data either has to include in their scope the work required to perform a manual impact analysis, or they duplicate the data and rebuild over again.  For many organizations this process perpetuates with the end result being thousands of siloed systems with high costs to maintain.
* **Data without trust and meaning** - If you have ever been in a meeting where there is more time spent debating the meaning of the data, rather than the insights that it provides, then you are aware of this problem.  If data cannot doesn't have clear definitions and detail of where it came from, it cannot be trusted, and will either not be used, or lead to poor decision making.  Auditing can add meaning and trust to data, it should tell users simply and clearly where there data came from.  

## What is an Auditable Data Framework

They key to an auditable data framework is **meaningful metadata**.  Metadata should be centralized, searchable, and readily available to all relevant staff (i.e. not just technology teams).  

By leveraging this metadata users should be able to:
* Attribute any cell or row of data to:
    * The process or job that loaded it, and the mappings and calculations contained within this job.
    * The data/time the row was applied.
    * The source table(s) or chain of source tables that the data came from.
    * Tables or areas the row was delivered to.
    
    This capability is commonly known as [data lineage](https://en.wikipedia.org/wiki/Data_lineage)
* Search/Browse Logical Definitions - Data columns have attributes that link to logical definitions or meanings of the row.  Some common examples are "name", "address", "balance", "cost price" etc.
* Search/Browse Business Domain - Data columns have attributes that link to a business domain.  Domains link the common attributes to an area of the business.  For example a field could have a logical definition of "name" and business domains of "employee", "customer", "supplier" etc.  This business domains often form a hierarchy that link to business owners and lines of business within the organization.


