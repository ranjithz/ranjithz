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



## Steps to validate the connection to a linux server :

    $ sudo su -

    $ yum install telnet     install telnet

    # telnet redistest.vnicjp.ng.0001.aps1.cache.amazonaws.com 6379   [ telnet copy Primary endpoint and remove the colon ":" before 6379  ]
  
![Image](https://user-images.githubusercontent.com/119755263/205637743-ad3381f8-3db4-4275-9884-6462dc326884.png)
------------------------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------------------
![Image](https://user-images.githubusercontent.com/119755263/205641477-2b0835eb-3452-4c0f-a1e4-a6b74e0444fd.png)
------------------------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------------------
