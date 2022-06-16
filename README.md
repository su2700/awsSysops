

## Welcome to Noah's AWS sysops 


1.An Aurora cluster is set up for an online shopping site.
The shopping cart component uses a reader endpoint as its target for displaying the products. 
A System Administrator finds the ReplicaLag metric is high. What effect would a customer encounter?

- [ ] a: Online shopping site would be very slow to respond

- [ ] b: Items in the shopping site may intermittently not reflect the complete shopping list

- [ ] c: Customer purchase order request would be delayed

- [ ] d: Customer purchase order request would be slow and may time out 


<details>
<summary>see answer</summary>
<pre><code>

Correct answer is B 
As the read replica is not able to keep up with the master, the items 
shown in the shopping site may not be the complete list from master. 
Refer AWS documentation - Aurora Replication Read scaling and high 
availability depend on minimal lag time. You can monitor how far an 
Aurora Replica is lagging behind the primary instance of your 
Aurora MySQL DB cluster by monitoring the Amazon CloudWatch ReplicaLag 
metric. Because Aurora Replicas read from the same cluster volume as 
the primary instance, the ReplicaLag metric has a different meaning 
for an Aurora MySQL DB cluster. The ReplicaLag metric for an Aurora 
Replica indicates the lag for the page cache of the Aurora Replica 
compared to that of the primary instance. Option A is wrong as there 
should be any impact on the shopping site performance Option C & D 
are wrong as there should not be any impact on customer transactions.
</code></pre>
</details>

2.A root account owner has created an S3 bucket testmycloud.
The account owner wants to allow everyone to upload the objects as well as enforce that 
the person who uploaded the object should manage the permission of those objects. Which 
is the easiest way to achieve this?

a: The root account owner should create a bucket policy which allows the IAM users to upload the object

b: The root account owner should create the bucket policy which allows the other account owners to set the object policy of that bucket

c: The root account should use ACL with the bucket to allow everyone to upload the object

d: The root account should create the IAM users and provide them the permission to upload content to the bucket.


<details>
<summary>see answer</summary>
<pre><code>

Correct answer is C 
as Each AWS S3 bucket and object has an ACL (Access Control List) associated with it. An ACL is a list of grants identifying the grantee and the permission granted. The user can use ACLs to grant basic read/write permissions to other AWS accounts. ACLs use an Amazon S3–specific XML schema. The user cannot grant permissions to other users in his account. ACLs are suitable for specific scenarios. For example, if a bucket owner allows other AWS accounts to upload objects, permissions to these objects can only be managed using the object ACL by the AWS account that owns the object. Option A is wrong as new policy and IAM user needs to be created every time. Option B is wrong as there is no object policy but only user & bucket policy Option D is wrong as we can create as policy for providing permission

</code></pre>
</details>
