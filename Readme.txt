1. Installed 2 application servers M4.

2. Installed Keepalived,HA proxy in both the servers for loan balancing. We can define servers as primary and secondary in keepalived.
	The keepalived gives an IP to the primary server and incase the primary server is down the secondary server will get the IP.(i.e if the 
	primary server is down the secondary server will be up automatically without any disturbance).
	
	If we are deploying application(production environment) in one node then the other node is still up and available to clients. After the 
	deployement is success in one node the then we can deploy it on other node.

3. Install Nginx for proxy passing.

4. Used API to upload and download images from CDN. When we have to upload/ download any images in application we call an API through which we can
	upload or download images in CDN.

5. Installed database with Merge replication(two way replication.).
	To case of DR we can use database mirroring.


note:
Varnish can be used as cache server. 


Why this solution:

I have been using these steps in production environment (internet banking, BankSmart(mobile banking.))
It has zero downtime since it has two nodes. while updating one node other node is always available to clients.
