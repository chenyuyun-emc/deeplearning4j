---
title:
layout: default
---

Quick Start Guide
=========================================

## Prerequisites

This Quick Start guide assumes that you have the following already installed:

1. Java 7
2. An IDE like IntelliJ
3. [Maven](../maven.html) (Automated build tool)
4. [Canova](../canova.html) (ML Vectorization lib)
 
If you need to install any of the above, please read how in this [Getting Started guide](http://nd4j.org/getstarted.html).

## DL4J in 5 Easy Steps

After those installs, if you can follow these five steps, you'll be up and running:

1. *git clone* [the examples](https://github.com/deeplearning4j/dl4j-0.0.3.3-examples). We are currently on version 0.0.3.3.x
2. Import the examples as a project into IntelliJ with Maven
3. Pick a Blas [backend](http://nd4j.org/dependencies.html), paste it in your POM.xml file (Start with *nd4j-jblas*) and make sure you have the latest version of ND4J in the properties (we're on 0.0.3.5.5.x).
4. Select example from the lefthand file tree (Start with *DBNIrisExample.java*)
5. Hit run! (It's the green button)

You should get an F1 score about about 0.60, which is good for a small dataset like Iris.

Once you do that, try the other examples. 

## Dependencies and Backends

Blas backends are what power the linear algebra operations behind DL4J's neural nets. GPUs require the Jcublas backend, while CPUs work with Jblas and Netlib Blas. You can find all of them on [Maven Central](https://search.maven.org); click the linked version number under "Latest Version"; copy the dependency code on the left side of the subsequent screen; and paste it into your project root's pom.xml in IntelliJ.

Your Blas backend will look something like this:

     <dependency>
       <groupId>org.nd4j</groupId>
       <artifactId>nd4j-jblas</artifactId>
       <version>${nd4j.version}</version>
     </dependency>

For core algorithms, you can simply add this snippet to your deeplearning4j POM.xml file:

     <dependency>
         <groupId>org.deeplearning4j</groupId>
         <artifactId>deeplearning4j-core</artifactId>
         <version>${deeplearning4j.version}</version>
     </dependency>