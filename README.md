# ClusterMapper
Java application to map the result from two or more clustering steps. e.g., First, dereplication of sequencing reads and uclust or swarm afterward.   

**Usage**: `java -cp build/classes clustermapper.ClusterMapper <mode> [options]`


**Modes:** 
* _uc2uc_: Map two different uc files. i.e. First uc file from dereplication and the second one from the OTU picking. Usefull for methods like uclust, vsearch, swarm, etc.
* _uc2otu_: Map a uc file and the second clustering should be a OTU map on txt format. i.e QIIME output from pick_otus.py script


### Example 

@Project repository

`java -cp build/classes clustermapper.ClusterMapper uc2uc -uc dereplicate/derep.reads.uc -uc2 swarm_out/swarms.uc -o abundance.txt --otu-tbl -samd \#  --full-uc`

For all available options: 

**Help menu**:  `java -cp build/classes clustermapper.ClusterMapper`
