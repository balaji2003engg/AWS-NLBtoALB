# Hosted application on  EC2  servers and ALB is configured as  internal(private) but needs to access the hosted application to access to the public without modifying the exisitng one.


Solution:

1. Create the target group to point out the ALB 
2. Create the NLB with above created the target group.
3. Modify securiy groups of ALB to access the public 
4. Make sure that update listensers of ALB with public listed domains

EC2---------------> ALB <------------------------  NLB ( Public)
    Private                   Priavte
    
    
#Reference Link
https://aws.amazon.com/blogs/networking-and-content-delivery/application-load-balancer-type-target-group-for-network-load-balancer/
