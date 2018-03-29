# spark-wordcount

Running a WordCount Program with PySpark 

# 1.Prerequisites : Single-Node Hadoop Cluster with Pydoop
	1.1. Ubuntu 12.10, 64-bit desktop version
	
	1.2. Oracle Java 8
			Install from command line :
			sudo add-apt-repository ppa:webupd8team/java
			sudo apt-get update
			sudo apt-get install oracle-java8-installer  
		
	1.3. Hadoop 2.7.4
			Download from : http://hadoop.apache.org/releases.html

	1.4. Spark 2.2.0 for Hadoop 2.7.*
			Download from : https://spark.apache.org/downloads.html
		
# 2. Start Spark
	2.1. Start hadoop from hadoop folder line : 
			./start-all.sh
	2.2. Check processes by running jps
			DataNode
			NameNode
			SecondaryNameNode
			TaskTracker
			JobTracker
			JPS
	2.3. Start PySpark from inside spark folder :
			./bin/pyspark
	
# 3. Running WordCount
	3.1. Create input and output directories on hdfs
			hdfs dfs -mkdir ~/input/
			hdfs dfs -mkdir ~/output/
	3.2. Save input.txt to ~/input/
			hdfs dfs -copyFromLocal input.txt /input
	3.3. Run WordCount.txt in pyspark shell.
	3.4. Output will be available at hdfs://localhost:9000/output/output.txt
	
	
