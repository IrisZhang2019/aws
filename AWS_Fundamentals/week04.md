### Monitoring and Scalability

#### CloudWatch
用于检测各种service

#### ELB (Elastic Load Balancer)
launched in vpc  
有request level（Layer 7）的Application LB来分HTTP或HTTPS的traffic  
也有connection level（Layer 4）的Network LB分TCP的traffic

#### AutoScaling
由CloudWatch监视，如果load过大就会auto scale  
在EC2下选Auto Scaling Group  
what to launch: 选择config，可以和EC2输入相同  
where to launch: 选VPC，subnet，ELB，
how to launch: 选instance个数上下限，average CPU utilization等
