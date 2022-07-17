# Election_Analysis
To view the results first hand, please click this link to access the Text File with the findings: [Python Challenge - Election Analysis](https://github.com/yaakoum/Election_Analysis/blob/main/election_analysis.txt)

## Overview of Election Audit
Colorado Board of Elections employee, Tom, has come to request for our assistance as we have become well rounded Python users. He needs our skills report the finding for the election and to audit the tabulated results for U.S. congressional precinct in Colorado. Some of the things we will be auditing are the name of the candidates and their votes and percentage of the total votes as well as distinguishing the winner by popular vote. Some additional information that we will provide in our audit will indicate each precincts' activity and the leading county with the highest turnout.

## Election-Audit Results
As menioned in the overview, there were many things we were tasked to do. We were requested to find multiple conclusions and below you will find all the information to do with our audit. Here is a picture of the results to make it easier in viewing:

<img src="https://github.com/yaakoum/Election_Analysis/blob/main/Final%20Results.png" width="430" height="500" />   

1. **_How many votes were cast in this congressional election?_** <br /> The total number of votes that were cast in this congressional election were: 369,711
2. **_Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct._** <br /> As you can tell by the image above, the highest turnout was in Denver by a long shot with over 80% (306,055 of 369,711) of the votes coming out from there. Jefferson and Arapahoe both had very little turnout compared to Denver with each of them accounting for only only 10.5% and 6.7% respectively of all votes.
3. **_Which county had the largest number of votes?_** <br /> As mentioned Denver had the largest number of votes with over 80% (306,055 of 369,711) of them coming from here.
4. **_Provide a breakdown of the number of votes and the percentage of the total votes each candidate received._** <br /> Funny enough, there was a similar disparity in the results between the candidates and the county. With 73% of the votes going to Diana DeGette, she won the election with the a popular vote total of 272,892 votes. She was followed by Charles Casper Stockham with 23% of the popular vote and Raymon Anthony Doane coming in last with a dissapointing 3.1% of the votes.
5. **_Which candidate won the election, what was their vote count, and what was their percentage of the total votes?_** <br /> With 73% of the votes going to Diana DeGette, she won the election with the a popular vote total of 272,892 votes. 

## Election-Audit Summary
Generally speaking the code we were able to formulate here is largely transferable and ready to be used for other elections. There are a few small things to keep in mind to ensure it will work with no hiccups and they are listed below.
- The first thing has to do with the file location. As you can see in the code below as an example, the file that the audit is referencing is something on my computer specifically and for this to work elsewhere that would need to be adjusted to wherever the file is being referenced.

        Add a variable to load a file from a path.
        file_to_load = os.path.join("Resources", "election_results.csv")
        Add a variable to save the file to a path.
        file_to_save = os.path.join("analysis", "election_analysis.txt")   
 
- The second consideration would have to do with the CSV format. To ensure the smoothest and simplist experience when replicating the audit for other elections, the column and data orientation in general should follow the same style with a long list of all ballots then city then candidate. If there are differences the following codes would need modifying:

         # For each row in the CSV file.
      for row in reader:

        # Get the candidate name from each row.
        candidate_name = row[2]

        # 3: Extract the county name from each row.
        county_name = row[1]
