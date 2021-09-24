# EXTRACTION-OF-HIGH-UTILITY-PATTERNS-BASED-ON-TIME-INTERVALS-AND-UTILITY-VS-TIME-INTERVAL-RELATIONSHIp
Step 1: To build the code
Open using IntelliJ IDEA.On the right side click on “maven”.Then click on “m” and use command “mvn package ” to build the jar.The location of jar will be shown on console below i.e. basically the in “target” subdirectory of parent folder.

Note 2: Run the code
The jar file is stored in “target folder” of jar file Project_2020.jar whose link is shared
To Run Sequence Generation Code
hadoop jar BigData.jar  DHUTISP  <input directory in HDFS> <min_util>
To Run Clustering Code
hadoop jar BigData.jar KMeans <input file> <output file>
NOTE: The system should have Hadoop along with yarn(any version>=3.0.3) configured.And the jdk for version 8 or higher should be there
The input file should be there in HDFS. The commands are as follows:
bin/hdfs dfs -mkdir input
bin/hdfs dfs -put <input-files> input

Note 3:Format of input file
1.For the sequence generation code:
 each line of the input file contains a sequence in the following format:-
<SID>:<Space separated List of items in the order they appear in the sequence>:<space separated Timestamps in order>:<space separated Utilities in order>:<Total utility of sequence>
2.For clustering the format is<sequence>:<utility>(The output of previous code)
