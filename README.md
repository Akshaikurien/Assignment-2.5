# Assignment-2.5

1.Cluster and Hadoop cluster

Cluster
A computer cluster is a single logical unit consisting of multiple computers that are linked through a LAN. The networked computers essentially act as a single, much more powerful machine. A computer cluster provides much faster processing speed, larger storage capacity, better data integrity, superior reliability and wider availability of resources. Computer clusters are, however, much more costly to implement and maintain. This results in much higher running overhead compared to a single computer
The major advantages of using computer clusters are clear when an organization requires large scale processing. When used this way, computer clusters offer: Cost efficiency: the cluster technique is cost effective for the amount of power and processing speed being produced. It is more efficient and much cheaper compared to other solutions like setting up mainframe computers. Processing speed: multiple high speed computers work together to provided unified processing, and thus faster processing overall. Improved network infrastructure: different LAN topologies are implemented to form a computer cluster. These networks create a highly efficient and effective infrastructure that prevents bottlenecks. Flexibility: unlike mainframe computers, computer clusters can be upgraded to enhance the existing specifications or add extra components to the system. High availability of resources: If any single component fails in a computer cluster, the other machines continue to provide uninterrupted processing. This redundancy is lacking in mainframe systems.

Hadoop Cluster

A Hadoop cluster is a special type of computational cluster designed specifically for storing and analyzing huge amounts of unstructured data in a distributed computing environment. Such clusters run Hadoop's open source distributed processing software on low-cost commodity computers. Typically one machine in the cluster is designated as the NameNode and another machine the as JobTracker; these are the masters. The rest of the machines in the cluster act as both DataNode and TaskTracker; these are the slaves. Hadoop clusters are often referred to as "shared nothing" systems because the only thing that is shared between nodes is the network that connects them. 
Hadoop clusters are known for boosting the speed of data analysis applications. They also are highly scalable: If a cluster's processing power is overwhelmed by growing volumes of data, additional cluster nodes can be added to increase throughput. Hadoop clusters also are highly resistant to failure because each piece of data is copied onto other cluster nodes, which ensures that the data is not lost if one node fails.
As of early 2013, Facebook was recognized as having the largest Hadoop cluster in the world. Other prominent users include Google, Yahoo and IBM.


2.Rack and rack arrangement in a hadoop cluster

A Node is simply a computer. This is typically non-enterprise, commodity hardware for nodes that contain data. Storage of Nodes is called as rack. A rack is a collection of 30 or 40 nodes that are physically stored close together and are all connected to the same network switch. Network bandwidth between any two nodes in rack is greater than bandwidth between two nodes on different racks. A Hadoop Cluster is a collection of racks.

Hadoop Cluster would consists of

·        110 different racks
·        Each rack would have around 40 slave machine
·        At the top of each rack there is a rack switch
·        Each slave machine(rack server in a rack) has cables coming out it from both the ends
·        Cables are connected to rack switch at the top which means that top rack switch will have around 80 ports
·        There are global 8 core switches
·        The rack switch has uplinks connected to core switches and hence connecting all other racks with uniform bandwidth, forming the Cluster
·        In the cluster, few machines to act as Name node and as JobTracker. They are referred as Masters. These masters have different configuration favoring more DRAM and CPU and less local storage.
·        The majority of the machines acts as DataNode and Task Trackers and are referred as Slaves. These slave nodes have lots of local disk storage and moderate amounts of CPU and DRAM

