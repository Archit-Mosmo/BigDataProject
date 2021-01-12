# BigDataProject

As a part to submit a project in my course timeperiod. I have made a simple mapper reducer function of matrix multiplication. As matrix have some property so it need a special set of multiplication rules. And also I'm sharing my Hadoop code for better understanding.

#### File Transfer from Local to Hadoop Cluster

hdfs dfs -put /home/archit/Matrix_1.txt  /archit/Task_1

hdfs dfs -put /home/archit/Matrix_2.txt  /archit/Task_1

###### Now File got transfered from local system to Hadoop Cluster. Time to run mapper and reducer files on these files.

#### Mapper Reducer part

hadoop jar /usr/local/hadoop/hadoop-2.9.2/share/hadoop/tools/lib/hadoop-streaming-2.9.2.jar -file /home/archit/mapper_Matrix.py -mapper /home/archit/mapper_Matrix.py -file /home/archit/reducer_Matrix.py -reducer /home/archit/reducer_Matrix.py -input /archit/Task_1/Matrix_1.txt -input /archit/Task_1/Matrix_2.txt -output /Matrix_Mult

###### Result is success.
