Memo for コードで学ぶAWS入門

Chapter 3 

计算
- EC2: 最常用
- Lambda: Function as a Service, Severless

Storage
- EBS: 连EC2的，类似于file system一样的
- S3 (Simple Storage Service): Object storage, serverless

Region & AZ
- Region: 不同region的服务互相隔离
- AZ: 为防止停电等突发事态而在每个region会有两个以上AZ，AZ之间传送很快，基本不需要在意用了哪一个AZ

AWS CLI, CloudFormation, AWS CDK
- AWS CLI: 可以用来管理infra (eg 建立一个EC2)，也可以用来管理task (eg 在EC2里面更新一段代码)，前者一般用CloudFormation管理
- CloudFormation是基于JSON的配置文件，可由AWS CDK (Cloud Development Kit)通过代码语言生成。Python使用aws_ckd

