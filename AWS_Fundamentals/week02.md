#### 建立VPC，放个public subnet，并在里面放EC2
VPC (Virtual Private Cloud)

VPC里面有subnets

subnets主要用determine access to gateways，ingress/egress

建立VPC
- 需要定义private IP range
- 给它命名
- subnet将使用里面的一部分IP range
- 需要选择Availability Zone

（Q：随便建一个VPC可以吗）

（Q：什么叫private IP range）

建立Internet Gateway (IGW)，使之于VPC相连，建立route table与subnet相连

建立IGW
- 给它一个名字
- 建立后与VPC连接

建立route table
- 给它一个名字
- 选择VPC
- 建立后添加Destination到0.0.0.0，target为VPC，允许外部访问
- 之后添加subnet的association
（Q：不是太懂route table）

最后在subnet里面放个EC2

#### 在另一个private subnet里面放DB

在里面放个RDS

将两个subnets连在一起，但是这个private subnet不接IGW

#### 在同一个VPC的不同Availability Zone里分别建一个public和private subnet

把route table加上public subnet associate

在public subnet里加新的EC2

在private subnet里加Multi-AZ ADS
（在今后的章节）

#### 加个elastic load balancer (ELB)
两个public subnet用ELB连起来

ELB在EC2的dashboard下面

建立ELB
- 需要选择type，暂时选Application LB
- 给它个名字
- Listeners port 80
- 选择VPC，AZ下的两个public subnet
- Security Group选择
- Routing命名，register targets选两个EC2

#### 加个virtual private gateway (VGW)
可以不通过IGW连接到里面，比如说自己的server通过VPN连接到VGW




