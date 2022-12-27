## ELASTIC LOAD BALANCER - ELB

Creating two EC2 servers ex: ELB-1-reliance, ELB-2-sony

Installing apache to both ec2 servers

$ yum install httpd

& ls -lrt

$ cd /var/wwww/html/

$ mkdir reliance

$ cd reliance
 
$ vi index.html

 ![image](https://user-images.githubusercontent.com/119755263/209655348-a5d2627d-991e-4d03-aef3-9888d2b7634b.png)

$ systemctl enable httpd   " to run httpd package"


Hit the respective public dns of each server to the browser

apache test page will be displayed with reliance in server-1 ( ELB-1-reliance ) 

![image](https://user-images.githubusercontent.com/119755263/209641906-2fccd0f2-9bec-4298-b691-0079d3745412.png)

similary do the same steps in next serer andHit the public dns to the respective browser

apache test page will be displayed with sony in server-2 ( ELB-2-sony )

![image](https://user-images.githubusercontent.com/119755263/209642928-5e34e0bf-818c-406d-8bc6-1a498c7ed41f.png)

Please check the security inbound rules if the ports are enabled or not , if not add rule , htttp , anywhere ipv4 then save the rule and restart the apache

$ sysytemctl restart httpd


## Creating 2 target group

Add health check for reliance

 ![image](https://user-images.githubusercontent.com/119755263/209644580-3a2e0566-b7f2-48e1-9233-13c84fb28438.png)

click Include as pending below with first ELB-1-RELIANCE 

![image](https://user-images.githubusercontent.com/119755263/209646052-a090b7d8-9910-4573-956e-97785623e4d6.png)

Now summary of first target group is shown and create target group 1

![image](https://user-images.githubusercontent.com/119755263/209646379-6a9f870e-ecb8-4839-8832-1844db7e0b39.png)

simirlarly in second server Add health check for sony

![image](https://user-images.githubusercontent.com/119755263/209645528-3fab5676-9642-456a-9913-29dd71e8f896.png)

click Include as pending below with second ELB-2-sony

![image](https://user-images.githubusercontent.com/119755263/209647256-6ebd189b-be66-4090-b2aa-9071f305786f.png)

Finally 2 target groups are created

![image](https://user-images.githubusercontent.com/119755263/209648022-39e78bb8-5556-4c73-83e4-550cb8dd3584.png)


## Create a load balancer

![image](https://user-images.githubusercontent.com/119755263/209638236-b972b60a-3e75-40c2-a8e4-c29e9c85d923.png)

select the load balancer 

![image](https://user-images.githubusercontent.com/119755263/209649673-a96927c1-70fd-4158-b954-8dd71f79fbf7.png)

Go to rules 

![image](https://user-images.githubusercontent.com/119755263/209649929-e5304dba-c52e-4918-b52b-45b40f34d97d.png)

Go to manage rules

Select add rule , then insert rule , path  /relance* , 1. Forward to...  elb1-reliance , then save

![image](https://user-images.githubusercontent.com/119755263/209650618-22c73b1c-8d84-42c6-9a2f-1765af3eb8d0.png)

Similarly Select add rule , then insert rule , path  /sony* , 1. Forward to...  elb2-sony , then save

![image](https://user-images.githubusercontent.com/119755263/209651588-b3f2f47c-f272-44fa-b001-2275a411fa15.png)

Now copy public dns and hit on the browser anlong with bmnmmnmnmnmn.compute.amazonaws.com/reliance/index.html

![image](https://user-images.githubusercontent.com/119755263/209652535-e11cd5fd-d4e5-4eaa-94dd-e14a52a7c2ca.png)

Now copy public dns and hit on the browser anlong with /sony/index.html

![image](https://user-images.githubusercontent.com/119755263/209653135-eed75ffd-2265-4e64-9779-56c81f3df3ca.png)




