# Winning Baseball Games in the RMAC
Final Project for Regis University Data Science Practicum II - Spring 2019

The Rocky Mountain Athletic Conference is an NCAA division II athletic conference with team located in various states in the Rocky Mountain region. The conference has had anywhere from eight to ten baseball teams since 2004 with all teams having the same goal: win baseball games. As the leader of the team, the head coach must make decisions that will lead to the team to victory in games with many of these decisions surrounding what the team will work on during practice, and what kind of player will be recruited to join the team in years to come. As such, it would be helpful for a coach to know which aspects of a baseball game most contribute to the outcome of a win. Overall, there are three aspects of the game, batting, fielding, and pitching. Within each of these three broad categories are subcategories that measure statistics such as batting average or earned run average. If a coach were to know which of these categories most contributed to teams winning baseball games within their respective conferences, then the coach would be able to tailor practices to work on these specific aspects of the game, and also know which type of player needs to be recruited for the future. This goal of this project is to uncover which statistical categories most contribute to winning baseball games in the RMAC so that the coaches of the Regis University baseball team may be able to use the information to supplement future decisions. 

## Data Collection and Cleaning

The RMAC baseball archives keep statistics that date back to the 2004 season. I collected all team statistics available on the RMAC website from years 2004-2018. The team statistics were divided into three categories that included “overall statistics”, “pitching statistics”, and “fielding statistics”. The “pitching statistics” category and the “fielding statistics” category contained unique measures, however the “overall statistics” category did contain some repeat statistics. I downloaded all the data sets from the RMAC website and loaded them into excel spreadsheets. I was able to use the “text-to-columns” function in excel to get the data into the proper format in excel, and then converted my excel worksheet into a csv file. 
Most of the cleaning that was necessary for this project was done in excel. The cleaning in excel included combining the yearly data into a single worksheet and then ensuring that the formatting of the single combined spreadsheet was acceptable for use. Once cleaning in excel was complete, I saved the worksheet as a csv file and uploaded it into Rstudio to begin work on the data. In total, the data set is comprised of 123 rows of 56 variables(columns) for a total of 6,888 total observations. All variables expect one are numeric. One of the variables is also the dependent variable that I will be attempting to predict. This leaves 53 variables that will be used for prediction. The acronyms for the variables in the data are as follows:

## Batting Statistics

AVG: Batting Average,
G: Games Played,
AB: At-bats,
R: Runs scored,
H: Hits,
DOUBLES (originally 2B): Doubles,
TRIPLES (originally 3B): Triples,
HR: Homeruns,
RBI: Runs Batted In,
TB: Total Bases,
SLGperc: Slugging Percentage,
BB: Base on Balls (Walks),
HBP: Hit by Pitch,
SO: Strikeouts,
GDP: Ground Ball Doubles Plays Hit Into,
Obperc: On-base percentage,
SF: Sacrifice Flies,
SH: Sacrifice Hits,
SBB: Stolen Bases,
ATT: Stolen Base Attempts,
SBB-ATTperc : Stolen Base percentage

## Pitching Statistics

ERA: Earned Run Average,
W: Team Wins,
CG: Complete Games,
SHO: Shutouts,
CBO: Complete Game Shutouts,
SV: Saves,
IP: Innings Pitched,
Hallowed: Hits allowed,
Rallowed: Runs allowed,
ER: Earned Runs,
BBallowed: Walks allowed,
SOfor: Number of strikeouts thrown,
DOUBLESAllowed: Doubles Allowed,
TRIPLESAllowed: Triples Allowed,
HRAllowed: Home Runs Allowed,
ABagainst: At-bats against,
AVGagainst: Batting average against,
WP: Wild Pitches,
HBPpithcing: Number of batters hit by a pitch,
BK: Balks,
SFA: Sacrifice Flies Against,
SHA: Sacrifice Hits Against

## Fielding Statistics

C: Chances,
PO: Put-outs,
A: Assists,
E: Errors,
FLDperc: Fielding Percentage,
DPs: Double Plays Turned,
SBA: Stolen Bases Allowed,
CSB: Caught Stealing By (pitcher and catcher),
SBAperc: Stolen Bases Allowed percentage,
PB: Passed Balls,
CI: Catcher’s Interference,
