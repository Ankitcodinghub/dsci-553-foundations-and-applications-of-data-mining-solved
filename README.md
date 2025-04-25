# dsci-553-foundations-and-applications-of-data-mining-solved



**<span style='color:red'>TO GET THIS SOLUTION VISIT:</span>** https://www.ankitcodinghub.com/product/dsci-553-foundations-and-applications-of-data-mining-solved-3/

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;131363&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;DSCI-553 Foundations and Applications of Data Mining Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">
            
<div class="kksr-stars">
    
<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
    
<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>
                

<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
Assignment 4

1. Overview of the Assignment

In this assignment, you will explore the spark GraphFrames library as well as implement your own Girvan-Newman algorithm using the Spark Framework to detect communities in graphs. You will use the ub_sample_data.csv dataset to find users who have a similar business taste. The goal of this assignment is to help you understand how to use the Girvan-Newman algorithm to detect communities in an efficient way within a distributed environment.

2. Requirements

2.1 Programming Requirements

a. You must use Python and Spark to implement all tasks. There will be a 10% bonus for each task if you also submit a Scala implementation and both your Python and Scala implementations are correct.

b. For task1, you can use the Spark DataFrame and GraphFrames library. For task2 you can ONLY use

Spark RDD and standard Python or Scala libraries.

2.2 Programming Environment

Python 3.6, JDK 1.8, Scala 2.12, and Spark 3.1.2

We will use these library versions to compile and test your code. There will be no point if we cannot run your code on Vocareum. On Vocareum, you can call `spark-submit` located at

/opt/spark/spark-3.1.2-bin-hadoop3.2/bin/spark-submit`. (*Do not use the one at

`/home/local/spark/latest/bin/spark-submit (2.4.4))

2.3 Write your own code

Do not share code with other students!!

For this assignment to be an effective learning experience, you must write your own code! We emphasize this point because you will be able to find Python implementations of some of the required functions on the web. Please do not look for or at any such code!

2.4 What you need to turn in

You need to submit the following files on Vocareum:

a. [REQUIRED] two Python scripts, named: task1.py, task2.py

b1. [OPTIONAL, REQUIRED FOR SCALA] two Scala scripts, named: task1.scala, task2.scala b2. [OPTIONAL, REQUIRED FOR SCALA] one jar package, named: hw4.jar

c. [OPTIONAL] You can include other scripts called by your main program.

d. You don’t need to include your results. We will grade your code with our testing data (data will be in the same format).

3. Datasets

We have generated a sub-dataset, ub_sample_data.csv, from the Yelp review dataset containing user_id and business_id. You can find the data on Vocareum under resource/asnlib/publicdata/.

4. Tasks

4.1 Graph Construction

To construct the social network graph, assume that each node is uniquely labeled, and that links are undirected and unweighted.

Each node represents a user. There should be an edge between two nodes if the number of common businesses reviewed by two users is greater than or equivalent to the filter threshold. For example, suppose user1 reviewed set{business1, business2, business3} and user2 reviewed set{business2, business3, business4, business5}. If the threshold is 2, there will be an edge between user1 and user2.

If the user node has no edge, we will not include that node in the graph.

The filter threshold will be given as an input parameter when running your code.

4.2 Task1: Community Detection Based on GraphFrames (2 pts)

4.2.1 Execution Detail

The version of the GraphFrames should be 0.6.0.

(For your convenience, graphframes0.6.0 is already installed for python on Vocareum. The corresponding jar package can also be found under $ASNLIB/public folder. ) For Python (in local machine):

● [Approach 1] Run “python3.6 -m pip install graphframes” in the terminal to install the package.

● [Approach 2] In PyCharm, you add the sentence below into your code to use the jar package os.environ[“PYSPARK_SUBMIT_ARGS”] = “–packages graphframes:graphframes:0.8.2-spark3.1-s_2.12 pyspark-shell”

● In the terminal, you need to assign the parameter “packages” of the spark-submit:

–packages graphframes:graphframes:0.8.2-spark3.1-s_2.12 For Scala (in local machine):

● In Intellij IDEA, you need to add library dependencies to your project

“graphframes” % “graphframes” % “0.8.2-spark3.1-s_2.12”

“org.apache.spark” %% “spark-graphx” % sparkVersion

● In the terminal, you need to assign the parameter “packages” of the spark-submit:

–packages graphframes:graphframes:0.8.2-spark3.1-s_2.12

For the parameter “maxIter” of the LPA method, you should set it to 5.

4.2.2 Output Result

In this task, you need to save your result of communities in a txt file. Each line represents one community and the format is:

‘user_id1’, ‘user_id2’, ‘user_id3’, ‘user_id4’, …

Your result should be firstly sorted by the size of communities in the ascending order and then the first user_id in the community in lexicographical order (the user_id is type of string). The user_ids in each community should also be in the lexicographical order.

If there is only one node in the community, we still regard it as a valid community.

Figure 1: community output file format

4.3 Task2: Community Detection Based on Girvan-Newman algorithm (5 pts)

In task2, you will implement your own Girvan-Newman algorithm to detect the communities in the network graph. You can refer to the Chapter 10 from the Mining of Massive Datasets book for the algorithm details.

Because your task1 and task2 code will be executed separately, you need to construct the graph again in this task following the rules in section 4.1.

For task2, you can ONLY use Spark RDD and standard Python or Scala libraries. Remember to delete your code that imports graphframes. Usage of Spark DataFrame is NOT allowed in this task.

4.3.1 Betweenness Calculation (2 pts)

In this part, you will calculate the betweenness of each edge in the original graph you constructed in 4.1. Then you need to save your result in a txt file. The format of each line is

(‘user_id1’, ‘user_id2’), betweenness value

Your result should be firstly sorted by the betweenness values in the descending order and then the first user_id in the tuple in lexicographical order (the user_id is type of string). The two user_ids in each tuple should also be in lexicographical order.

For output, you should use the python built-in round() function to round the betweenness value to five digits after the decimal point. (Rounding is for output only, please do not use the rounded numbers for further calculation)

IMPORTANT: Please strictly follow the output format since your code will be graded automatically. We will not regrade because of formatting issues.

Figure 2: betweenness output file format

4.3.2 Community Detection (3 pts)

You are required to divide the graph into suitable communities, which reaches the global highest modularity. The formula of modularity is shown below:

According to the Girvan-Newman algorithm, after removing one edge, you should re-compute the betweenness. The “m” in the formula represents the edge number of the original graph. The “A” in the formula is the adjacent matrix of the original graph. (Hint: In each remove step, “m”, “A”, “k_i” and “k_j” should not be changed). In the step of removing the edges with the highest betweenness, if two or more edges have the same (highest) betweenness, you should remove all those edges.

If the community only has one user node, we still regard it as a valid community.

You need to save your result in a txt file. The format is the same with the output file from task1.

4.4 Execution Format

Execution example:

Python:

spark-submit –packages graphframes:graphframes:0.8.2-spark3.1-s_2.12 task1.py &lt;filter threshold&gt;

&lt;input_file_path&gt; &lt;community_output_file_path&gt;

spark-submit task2.py &lt;filter threshold&gt; &lt;input_file_path&gt; &lt;betweenness_output_file_path&gt; &lt;community_output_file_path&gt; Scala:

spark-submit –packages graphframes:graphframes:0.8.2-spark3.1-s_2.12 –-class task1 hw4.jar &lt;filter threshold&gt; &lt;input_file_path&gt; &lt;community_output_file_path&gt; spark-submit –-class task2 hw4.jar &lt;filter threshold&gt; &lt;input_file_path&gt; &lt;betweenness_output_file_path&gt; &lt;community_output_file_path&gt; Input parameters:

1. &lt;filter threshold&gt;: the filter threshold to generate edges between user nodes.

2. &lt;input file path&gt;: the path to the input file including path, file name and extension.

3. &lt;betweenness output file path&gt;: the path to the betweenness output file including path, file nameand extension.

4. &lt;community output file path&gt;: the path to the community output file including path, file name andextension.

Execution time:

The overall runtime limit of your task1 (from reading the input file to finishing writing the community output file) is 400 seconds.

The overall runtime limit of your task2 (from reading the input file to finishing writing the community output file) is 400 seconds.

If your runtime exceeds the above limit, there will be no point for this task.

5. About Vocareum

a. Dataset is under the directory $ASNLIB/publicdata/, jar package is under $ASNLIB/public/

b. You should upload the required files under your workspace: work/, and click submit

c. You should test your scripts on both the local machine and the Vocareum terminal before submission.

d. During the submission period, the Vocareum will automatically test task1 and task2.

e. During the grading period, the Vocareum will use another dataset that has the same format for testing.

f. We do not test the Scala implementation during the submission period.

g. Vocareum will automatically run both Python and Scala implementations during the grading period.

h. Please start your assignment early! You can resubmit any script on Vocareum. We will only grade on your last submission.

6. Grading Criteria

(% penalty = % penalty of possible points you get)

a. You can use your free 5-day extension separately or together

(https://docs.google.com/forms/d/e/1FAIpQLSf6hpYzacaV2d1CJMZfrlE-xl9N6bLkJbhi7aFlAQcObGj0X w/viewform)

b. There will be 10% bonus for each task if your Scala implementations are correct. Only when your

Python results are correct, the bonus of Scala will be calculated. There is no partial point for Scala.

c. There will be no point if your submission cannot be executed on Vocareum.

7. Common problems causing fail submission on Vocareum/FAQ

(If your program runs seems successfully on your local machine but fail on Vocareum, please check these)

1. Try your program on Vocareum terminal. Remember to set python version as python3.6,

And use the latest Spark

/opt/spark/spark-3.1.2-bin-hadoop3.2/bin/spark-submit

2. Check the input command line format.

3. Check the output format, for example, the header, tag, typo.

4. Check the requirements of sorting the results.

5. Your program scripts should be named as task1.py task2.py.

6. Check whether your local environment fits the assignment description, i.e. version, configuration.
