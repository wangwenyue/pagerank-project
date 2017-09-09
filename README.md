# PageRank project

## Overview
In this project, I implemented a 
pagerank search tools based on Pagerank algorithm using Hadoop MapReduce and Java language.

## Main Steps

* Build a pagerank Libraray from wiki data sets.

* According to the transmition matrix build a relationship model between webpages.

* According to the pagerank matrix calculate the weight between webpages.

* Using teleporting to solve two edge case problems:Spider traps and Dead ends. 

* Using Python httpserver to show the result.

## Web Interface

Demo looks like


![](demo.gif)

## Deploy
First we need deploy a hadoop cluster on Docker, this cluster has one Masternode and two slavenodes. The whole project is based on the docker.


```
$ hadoop com.sun.tools.javac.Main *.java
$ jar cf ngram.jar *.class
$ hadoop jar pr.jar Driver /transition /pagerank /output 5 0.8
```

* args0: dir of transition.txt
* args1: dir of PageRank.txt
* args2: dir of unitMultiplication result
* args3: times of convergence
* args4: value of beta


