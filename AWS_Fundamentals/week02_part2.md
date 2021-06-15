### Storage

#### Object Storage

主要放图片视频等，一修改就全部修改

* S3 (Simple Sotrage Service): images or files, backups etc

Bucket

每个storage是一个bucket，会有endpoint URL，通过HTTP/HTTPS可以连接（权限可选择）

建立Bucket：(没有权限…)

命名，选Region即可建立。Upload上传，default为private

* Glacier

#### Block level storage

* EBS (Elastic Block Storage)：主要作为DB，EC2 instance等

EC2和EBS之间可以连接，互相之间运行ON/OFF独立。但只能和一个EC2相连接。

* EFS (Elastic File System)：file storage

在一个Region里可以连多个EC2，可以不在同一个VPC里，甚至连接到on premise server里





