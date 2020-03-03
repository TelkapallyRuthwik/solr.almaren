# Solr Connector

[![Build Status](https://travis-ci.com/music-of-the-ainur/solr.almaren.svg?branch=master)](https://travis-ci.com/music-of-the-ainur/solr.almaren)

```
libraryDependencies += "com.github.music-of-the-ainur" %% "solr-almaren" % "0.0.3-2-4"
```

Solr Connector was implemented using [https://github.com/lucidworks/spark-solr](https://github.com/lucidworks/spark-solr). The *Solr Connector* just works on Solr Cloud.
For all the options available for the connector check on this [link](https://github.com/lucidworks/spark-solr#configuration-and-tuning).

In order to execute it, you need to choose the [Spark-Solr connector](https://github.com/lucidworks/spark-solr#version-compatibility) version based on your Spark Version like below:

```
spark-shell --master local[*] --packages "com.github.music-of-the-ainur:almaren-framework_2.11:0.2.3-2-4,com.github.music-of-the-ainur:solr-almaren_2.11:0.0.3-2-4,com.lucidworks.spark:spark-solr:3.6.0" --repositories https://repo.boundlessgeo.com/main/
```


## Source and Target

```scala
import com.github.music.of.the.ainur.almaren.Almaren
import com.github.music.of.the.ainur.almaren.solr.Solr.SolrImplicit

val almaren:Almaren = Almaren("App Name")

almaren.builder.sourceSolr("collection","zkHost1:2181,zkHost2:2181",options)

almaren.builder.targetSolr("collection","zkHost1:2181,zkHost2:2181",options)

```
