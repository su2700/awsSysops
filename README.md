## Welcome to Noah's AWS sysops 


1.An Aurora cluster is set up for an online shopping site.
The shopping cart component uses a reader endpoint as its target for displaying the products. 
A System Administrator finds the ReplicaLag metric is high. What effect would a customer encounter?

- [] a: Online shopping site would be very slow to respond

- [] b: Items in the shopping site may intermittently not reflect the complete shopping list

- [] c: Customer purchase order request would be delayed

- [] d: Customer purchase order request would be slow and may time out 






<details>
<summary>see answer</summary>
<pre><code>

Correct answer is B 
As the read replica is not able to keep up with the master, the items shown in the shopping site may not be the complete list from master. Refer AWS documentation - Aurora Replication Read scaling and high availability depend on minimal lag time. You can monitor how far an Aurora Replica is lagging behind the primary instance of your Aurora MySQL DB cluster by monitoring the Amazon CloudWatch ReplicaLag metric. Because Aurora Replicas read from the same cluster volume as the primary instance, the ReplicaLag metric has a different meaning for an Aurora MySQL DB cluster. The ReplicaLag metric for an Aurora Replica indicates the lag for the page cache of the Aurora Replica compared to that of the primary instance. Option A is wrong as there should be any impact on the shopping site performance Option C & D are wrong as there should not be any impact on customer transactions.
</code></pre>
</details>
