## REDIS CACHE

Redis is an in-memory data structure store, used as a distributed, in-memory key–value database, cache and message broker, with optional durability.  Redis supports different kinds of abstract data structures, such as strings, lists, maps, sets, sorted sets, HyperLogLogs, bitmaps, streams, and spatial indices.

** The default port for Redis is 6379. 

## HOW TO CUTOM REDIS CLUSTER IN AWS ? 

1.To grant network ingress from an Amazon VPC security group to a cluster

2.Sign in to the AWS Management Console and open the Amazon EC2 console at https://console.aws.amazon.com/ec2/.

3.In the navigation pane, under Network & Security, choose Security Groups.

4.From the list of security groups, choose the security group for your Amazon VPC. Unless you created a security group for ElastiCache use, this security group will be named default.

5.Choose the Inbound tab, and then do the following:

6.Choose Edit.

7.Choose Add rule.

8.In the Type column, choose Custom TCP rule.

9.In the Port range box, type the port number for your cluster node. This number must be the same one that you specified when you launched the cluster. The default port for Redis is 6379.

10.In the Source box, choose Anywhere which has the port range (0.0.0.0/0) so that any Amazon EC2 instance that you launch within your Amazon VPC can connect to your     ElastiCache nodes.

11.Choose Save.When you launch an Amazon EC2 instance into your Amazon VPC, that instance will be able to connect to your ElastiCache cluster.