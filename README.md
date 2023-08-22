# Database-Reach-Over-Time
Pulling data from an old-structure snapshot table that captures information about counts and fields for members in our first party database each month.
The original table used to match the format of our database on our MySQL server, but we migrate to AWS Redshift a few years ago and the names and structure of the fields were changed, so using this table requires some alterations.
Additionally, two of the fields I need to use here are binary. AML12 and AML24 hold either a 0 or a 1 to indicate if the recency of the person in question is within the last 12 months or within the last 24, I want to be able to slice between 12 and 24 audiences in one field,so I unpivot the table to make AML12 and AML24 options within one field.
Lots of renaming involved in this SQL due to poor data governance in historical tables.
