本章介绍了几个services:

### EC2
[Elastic Compute Cloud](https://aws.amazon.com/ec2/)

建立instance前，需要设置以下几点
- 选择AMI(Amazon Machine Image): 用于定义config, 如操作系统以及instance大小容量等
- 需要选定VPC和subnet
- IAM role用于service之间的连接
- Advanced Details中，填写需要运行的代码
- tag，加Name
- security group设置

### Lightsail
设置比EC2少

只需要选OS，blueprint就可以


