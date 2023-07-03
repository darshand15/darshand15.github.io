---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---



<!---!
{% for post in site.projects reversed %}
  {% include archive-single.html %}
{% endfor %}
--->

Introduction

<a href="/projects/Capstone_project"> Capstone Project </a>

## Automated Parallelization of Source Code using Program Comprehension
  * A Research Project aimed at exploring methods to improve the performance of sequential source code by automatically converting it to its parallel equivalent, thereby ensuring efficient utilization of the underlying hardware
  * Implemented Intra-Function and Inter-Function Parallelism
  * Intra-Function parallelism was implemented using the concept of program comprehension that enabled us to identify the intent and the algorithm implemented in a particular code section and consequently replace it with the optimized parallel version based on the defined mapping in the backend database
  * Inter-Function parallelism was implemented using a novel thread scheduling algorithm that enabled the parallel execution of the different functions in the original sequential program
  * Implemented as part of the Capstone Project during my Undergraduate Study

## Generic Programming in C
  * A project aimed at implementing Generic Programming features as a design pattern in C using pre-processor directives
  * Implemented generic containers - list, stack, queue, vector and hashmap supporting all the different data types
  * Implemented Iterators for each of these containers to decouple the containers and algorithms
  * Implemented Generic Algorithms like find, count, min, max, accumulate, etc that make use of the iterators
  * Implemented as part of the Design Patterns Course during my Undergraduate Study

## Implementation of Treaps
  * A project aimed at implementing the Treap as a generic data structure along with the different functionalities of a treap
  * Treap is a data structure that stores pairs (say [X,Y]) in a binary tree such that it is a binary search tree by X and a binary heap by Y
  * The entire treap and its individual nodes were built as generic canonical classes, thereby supporting all the different data types
  * Supported multiple operations such as insert node, delete node, split treap, merge two treaps, union, intersection, difference and traversal of treaps
  * Implemented a bidirectional iterator as a nested class within the treap class
  * Implemented multiple member algorithms such as find and replace
  * Implemented as part of the Generic Programming Course during my Undergraduate Study

## Mini Compiler for Python
  * A project aimed at implementing a mini compiler for the Python programming language supporting the different phases of a typical compiler, namely lexical analysis, syntax analysis, semantic analysis, intermediate code generation and intermediate code optimization
  * Supports the if, if-else, if-elif-else and for constructs, arithmetic, relational and logical operators, keywords, identifiers and various other features along with error detection and error handling mechanisms
  * Implemented as part of the Compiler Design Course during my Undergraduate Study

## Yet Another Centralized Scheduler (YACS)
  * A project aimed at implementing a centralised scheduling framework maintaining a master node and multiple worker nodes, all simulated as different processes on a single machine
  * The Master node receives job requests, which are scheduled on multiple slots across available worker machines
  * The Master process consists of separate threads to listen to requests, schedule map and reduce tasks and to listen to job completion information from workers, whereas the Worker process listens to job allocation information and simulates execution
  * Implemented 3 different scheduling algorithms, namely Least loaded, Round robin and Randomised.
  * Implemented as part of the Big Data Course during my Undergraduate Study

## Spacetime Trajectory Estimation
  * A project aimed at realizing the following in sequence:
    * Detecting and perceiving the relative depth of objects from a single camera using relative monocular depth perception
    * Recognizing the objects using YOLO Object Detection model
    * Tracking objects using a Multi Object Tracker and openCV
    * Simulating the events occurring after the end of the video in Unreal Engine by estimating the three-dimensional kinematic parameters of the objects
  * Provides better analysis of events through simulation
  * Implemented as part of the CDSAML Summer Internship

## Blockchain based Transaction System
  * Patient records and transaction details are stored on a decentralized ledger, enabling fast, secure and digitalised approach to organ/blood donation
  * Implemented as part of Hackathons

## Voice Based Grievance System
  * Developed an application to collect voice complaints, applied speech to text conversion on them and categorised and ranked them based on severity using the IBM Watson NLU
  * Provides for efficient response and timely resolution of grievances by the officials
  * Implemented as part of Hackathons


The link to the test video is as follows: 
<a href="/experience/#test_video_demo" target="_top">Video Demo</a>
