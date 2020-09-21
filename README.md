# Introduction

You've been invited to complete this data engineering design assignment.

We have deliberately designed this assignment to be open-ended in order to leave plenty of room for you 
to make choices. We do not expect you to spend days on this.  Simply provide your solution in a document 
that is at most 1 page long.

Good luck!

-Leap.

## Background

As a data engineer, you are requested to design a system to ingest, host and deliver meter data as efficiently as possible. 

Leap receives electricity meter data on a daily basis from utilities.  
- The size of the daily updates is a few Gb per day and updates are received roughly every 15 minutes. 
- The data arriving each day contains 3 types of updates:     
  a) new data for exsting meters from the last couple days    
  b) corrected data from previous days, and     
  c) historical and new data for new meters
- Only the most recent data is interesting -- incorrect past data must be saved but will rarely need to be accessed. 
- The total size of the data set is ~100gb but will grow by 50% every year. 

Business users need read access to the latest complete snapshot of the meter data. This snapshots contains: 
- The latest meter data, 
- Only the latest correct data (e.g. if we get a an update with correct data that ovewrwrites previous data, we only want to see the latest correct data)

With regards to the type of access, business users need to see visual graphs of meter usage, including the ability to choose the time range over which to plot the the meter data.
- Some business users also need to be able to run queries on the data and get results within minutes. 

Every month, we use the latest snapshot to produce settlement reports, which we send to our partners and are a key component of our revenue. The logic for these settlement reports 
is complex and requires a lot of (map-reduce) code to produce. 

## Assignment

**What stack would you recommend Leap uses to satisfy these requirements?**

Your solution should address the following core issues:

1) How and where should the data be stored? Why? 
2) We need daily access to a complete snapshot of the latest data. Given that we are continually receiving (incremental) updates, how should we create this snapshot? The snapshot
can be up to a day old.
3) The latest meter data should be available via a dashboard. What type of dashboard or front end would you recommend? Why? How does this dashboard access the data? 
4) Some of the organizations we work with will occasionally want to audit our reports at the end of the year. How can we make sure that we address any audit concerns? 

We are less interested in the fully worked-out details of a design and more interested in seeing if you've thought about all of the issues related to handling data. If you have 
experience with a particular aspect of this problem, please feel free to go into detail about your ideas!

Please provide your solution to this system along with your application to the data engineering position at Leap. We are looking forward to your design!

