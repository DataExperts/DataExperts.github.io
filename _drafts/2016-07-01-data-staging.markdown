---
layout: post
title:  "The importance of staging data"
date:   2016-07-01 18:00:00 +1000
author: Gary Holland
categories: updates
---

What is data staging, and why should it be an integral part of an organizations data strategy?

Data Staging
---

A data staging environment is one of the simplest and most effective ways for an organization to improve its data maturity.  The key attributes of a data staging environment are as follows:

* Data is stored in a raw format, meaning the data is structured in the same manner as the system that it was sourced from.
* Very limited data cleansing should be applied.  Exceptions to this rule might be simple filter to remove junk rows and columns, however cleansing and validation should not happen in a staging load.
* Where practical history should be retained, including tracking of change history.  Exceptions to this rule, might be due to privacy regulations or volume constraints.
* Auditing columns should be added to the staging tables to allow tracing of data back to the source system and data/time the data was created and updated.
* Data should be very carefully cataloged and documented.  This should describe the data and where it came from as well as linking to data owners and other stakeholders responsible for this data.

Creating a staging layer with these attributes is often skipped in favor of building point-point interfaces, which cherry pick the fields needed for each requirement.  The problem this causes, is when the next project comes along if the previously picked fields are not enough, they will need to go back to the systems, create `near` duplicate data.