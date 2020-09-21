# Introduction

You've been invited to complete this data engineering design assignment. We have deliberately designed this assignment to be open-ended in order to leave plenty of room for you to make choices. We do not expect you to spend days on this.  Simply provide your solution in a document that is at most 1 page long.

Good luck!

-Leap.

## Assignment

As a data engineer, you	are requested to design	a data lakehouse to ingest, host and deliver meter data as efficiently as possible.  

Leap receives electricity meter data on a daily basis from utilities.  The size of the daily updates are around a few GB.  The data arriving each day contains new meter data from the last 24 hours, as well as corrected data from previous days that should replace missing or inaccurate older meter data.  Once stored, business users would like access to a snapshot of the meter data, containing not only the latest data, but the most up-to-date data (ie those data from previous days that were corrected).   Their access could be a dashboard, where they would be able to select certain meters (e.g. via a meter-id), as well as choose the date range over which to plot the meter data.  Every month, we use the latest snapshot to produce settlement reports, which	we send	to our partners	and are a key component of our revenue.
What stack would you recommend Leap builds on the cloud to satisfy these requirements?

Your solution should address the following core issues:

1) Data	should be stored in a compressed format	(ie not ASCII tables).	What storage and/or file system should we use?
2) We should have a snapshot of	the latest data.  What type of job would produce these snapshots?  Please specify the stack you	would design and build, and why.
3) The latest meter data	should be available via	a dashboard.  What type of dashboard or front end would you recommend,	and why?
4) For the monthly settlement reports, we need to be able to identify which snapshot is	used to	create that report.  How would this data lineage be handled?

Please provide your solution to	this system along with your application	to the data engineering	position at Leap.  We are looking forward to your design!
