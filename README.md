# SupremeCourtJusticeDissentVotes
Dissenting Votes of Supreme Court Justices 1946-2019 from The Supreme Court Database
(1) Overview
 
Title: Dissenting Votes of Supreme Court Justices 1946-2019
 
Repository location:
https://github.com/lagypin/SupremeCourtJusticeDissentVotes

Paper Authors
1. Gypin, Lindsay.
 
Paper Author Roles and Affiliations
1. Author, University of Denver Morgridge College of Education.
 
Abstract
A dataset curated from the The Supreme Court Database Justice Centered data where the “majority” column listed “1,” indicating the Supreme Court Justice had cast a dissenting opinion vote on the case.  The data in this dataset represent every Supreme Court Justice dissenting opinion vote between the years 1946 and 2019.  The data are stored in a Microsoft Excel file on the Github Repository, and can be used to analyze dissenting opinion votes by Supreme Court Justices.  
 
Keywords
Dissent, Supreme Court, Justice, Vote

Context
This data was created to easily run statistical analyses on dissenting votes of Supreme Court Justices.
(1) Methods
 
Steps
I located a comprehensive database of Supreme Court decisions organized by Supreme Court Justice name provided by Washington University of Law. I downloaded the CSV file with 121,244 rows and 61 columns of information. For each case between 1946 and 2019, each of the nine justices has their own row. Each column represents data related to the vote, much of which is irrelevant for the scope of this project. I selected and deleted columns of extraneous information using Microsoft Excel. (Appendix A contains a comprehensive list of deleted columns.)  

Next, I used OpenRefine’s “Text filter” function to display only the rows in the “majority” column with a “1,” indicating the Justice cast a dissenting opinion. My dataset now has 20 columns and 22,467 rows. Though still a large dataset, this is a manageable size and provides information about dissenting opinions of Supreme Court Justices. 

Sampling strategy
I did not use sampling strategies, this is a comprehensive dataset based on available information provided by Washington University of Law.

Quality Control
Harold J Spaeth, funded by the National Foundation of Science, has collected and coded supreme court data and performed reliability checks on the data every term since the late 1980s. He also invites users of this publicly available dataset to email him if they notice any errors.  

Some Justices’ names were formatted with two initials capitalized and their last name capitalized, and others with only one initial. One Justice, Sandra Day O’Connor, had four capitals in her “justiceName” field (SDOConnor). I used the Text facet feature in OpenRefine to create a list of all possible choices (38), which I then renamed as “Firstname Lastname” or “Firstname Name Lastname” where relevant. Because I didn’t recognize every Justice’s name, I used Google to verify each datapoint. 

(2) Dataset description
 
Object name
SCDB_2019_01_justiceDissent.xlsx
 
Format names and versions
RBGDissents.xlsx
 
Creation dates
This dataset was curated between 2020-01-10 and 2020-03-10. 
 
Dataset Creators
Harold J. Spaeth Michigan State University College of Law, Lee Epstein Washington University in St. Louis, Andrew D. Martin University of Michigan Department of Political Science, Jeffrey A. Segal Stony Brook University Department of Political Science, Theodore J. Ruger University of Pennsylvania School of Law, and Sara C. Benesh University of Wisconsin-Milwaukee Department of Political Science are authors of the complete Supreme Court Database, Version 2019 Release 1. 
 
Language
English
 
License
CC BY-NC 3.0 US  

Data dictionary

Columns Names:
“caseid”
This is the first of four unique internal identification numbers. The first four digits are the term. The next four are the case within the term (starting at 001 and counting up).

“dateDecision”
This variable contains the year, month, and day that the Court announced its decision in the case.

“decisionType”
1	opinion of the court (orally argued)
2	per curiam (no oral argument)
4	decrees
5	equally divided vote
6	per curiam (orally argued)
7	judgment of the Court (orally argued)
8	seriatim

“chief”
This variable identifies the chief justice during whose tenure the case was decided.

“caseName”
This is the name of the case. 


“decisionDirection”
In order to determine whether the Court supports or opposes the issue to which the case pertains, this variable codes the ideological "direction" of the decision.

“authorityDecision1”
This variable and the next one (authorityDecision2) specify the bases on which the Supreme Court rested its decision with regard to each legal provision that the Court considered in the case.

“authorityDecision2”
See variable Authority for Decision 1 (authorityDecision1).

“lawType”
This variable and its components (lawSupp and lawMinor) identify the constitutional
provision(s), statute(s), or court rule(s) that the Court considered in the case.

“splitVote”
This variable indicates whether the vote variables (e.g., majVotes, minVotes) pertain to the vote on the first or second issue (or legal provision). 

“majVotes”
This variable specifies the number of justices voting in the majority; minVotes indicates the number of justices voting in dissent.

“minVotes”
This variable specifies the number of votes in dissent. Only dissents on the merits are specified in this variable

“justice”
This variable provides a unique identification number for each of the justices. Even though several justices served as both associate and chief justice they receive only one identification number.

“justiceName”
This is a string variable indicating the first initial for the five justices with a common surname (Harlan, Johnson, Marshall, Roberts, and White) and last name of each justice. 

“vote”
This variable provides information about each justice's vote in the case. 

“opinion”
This variable indicates the opinion, if any, that the justice wrote. 

“direction”
This variable indicates whether the justice cast a liberal or conservative vote. For the definitions of liberal and conservative, see variable decisionDirection. A missing value code indicates that the decisionDirection was unspecifiable or that that justice did not participate.

“majority”
Analysts commonly want to know the frequency with which given justices vote with the majority and/or in dissent overall or in certain sets of circumstances. This variable provides that information for each justice. Values: 1 = dissent; 2 = majority.

Rows
Each row illustrates one vote by one supreme court justice in one case.  

A full Codebook for The Supreme Court Database can be found online at: http://supremecourtdatabase.org/documentation.php?s=1

Repository name
Github
 
Publication date
2020-03-07
 
(3) Reuse potential

When a Supreme Court Justice disagrees with the majority vote, they cast a dissenting opinion.  These dissenting opinions can be used to later overrule Supreme Court decisions.  Justice Ruth Bader Ginsberg has recently become a popular culture icon for her dissenting opinions; with many liberals sporting tributes to the Justice’s famed “dissent collar.”  How often do Supreme Court Justices cast dissenting votes? Does Justice Ginsberg dissent more often than other Supreme Court Justices (the answer is no. Conservative Justice Scalia even cast more dissenting votes than Justice Ginsberg.) 

By isolating data related to dissenting opinion votes, it is possible to analyze the circumstances surrounding these votes.  Are liberal or conservative Justices more likely to cast dissenting votes?  Are dissenting votes more likely to occur during summer or winter months?  Historically, which Justice has cast the most dissenting opinions?  What are the most common reasons a Justice gives for casting a dissenting opinion? Etc. This curated dataset makes these analyses possible.

The chart below, created using the minVote column of data in this dataset, illustrates the number of Justices who cast dissenting opinion votes in cases where at least one dissenting opinion vote was cast.  In cases with at least one dissenting opinion vote, 24.8% had four dissenting opinion votes, 33.1% had three dissenting opinion votes, 23.1% had two dissenting opinion votes, and 18.9% had one dissenting opinion vote.  

Figure 1: Number of Dissent Votes Cast Per Case with Dissent Votes

Further disaggregation of the data related to the Justices may create more interesting analysis opportunities.  For example, Justice’s sex/gender and race/ethnicity are not currently included in the dataset, and may lead to interesting analysis.  Additionally, the curator of this dataset isn’t a legal expert and left many fields in the dataset that seemed relevant but upon analysis may prove irrelevant and can be deleted.  

When a Supreme Court Justice casts a dissenting opinion vote, they are able to add a note about why they are dissenting (in the “opinion” field.)  These opinions can be used in future cases to overturn decisions, or as reasons not to use the case as a seminal decision by which future cases can be determined.  A potential use for this dataset would be to organize this dataset by those opinions and the laws to which they relate.  Are Justices more likely to cast dissenting votes for cases related to certain types of laws?  Or are the dissenting opinions similar in such a way that indicates a law should be revised?  

Limitations of this dataset include the amount of data - it is unwieldy and those unfamiliar with OpenRefine might have a difficult time navigating it effectively.  Additionally, many of the columns of data are related to legal concepts that are difficult to understand, even after reading the detailed codebook provided by The Supreme Court Database.  
 
Acknowledgements
Washington University in St. Louis
 
Funding statement
This data was adapted from The Supreme Court Database which has been generously supported by the National Science Foundation.
 
References
Harold J. Spaeth, Lee Epstein, et al. 2019 Supreme Court Database, Version 2019 Release 1. URL: http://Supremecourtdatabase.org. 
Appendix A: List of Column Deleted from Dataset
docketid
respondent
partyWinning
caseissuesid
jurisdiction
precendentAlteration
voteid,
adminAction
issue
usCite
adminActionState
issueArea
sctCite
threeJudgeFdc
lawType
ledCite
caseOrigin
lawSupp
lexisCite
caseOriginState
lawMinor
term
caseSource
majOpinWriter
naturalCourt
caseSourceState
majOpinAssigner
docket 
lcDisagreement
firstAgreement
dateArgument
certReason
firstAgreement
dateRearg
lcDisposition
secondAgreement
petitioner
declarationUncon
dateArgument
petitionerState
caseDisposition
dateRearg

